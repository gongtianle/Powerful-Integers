//way
class Solution {
public:
    vector<int> powerfulIntegers(int x, int y, int bound) {
	vector<int> res;
	for (int i = 0; pow(x,i) <= bound; i++)
	{
		for (int j = 0; pow(x,i)+pow(y,j)<= bound; j++)
		{
			res.push_back(pow(x,i)+pow(y,j));
		}
	}
	sort(res.begin(), res.end());
	for (int i=1;i<res.size();i++)
		if (res[i-1]==res[i])
		{
			res.erase(res.begin() + i, res.begin() + i + 1);
			i--;
		}
	return res;
}
};

static int x = []() {std::ios::sync_with_stdio(false); cin.tie(0); return 0; }();
//way 2
class Solution 
{
public:
    vector<int> powerfulIntegers(int x, int y, int bound) 
    {
        unordered_set<int> set;
        int i = x == 1 ? bound : x;
        int j = y == 1 ? bound : y;
        for (int m = 1; m < bound; m *= i;
        {
            for (int n = 1; m + n <= bound; n *= j) set.insert(m + n);
        }
        return vector<int>(begin(set), end(set));

    }

};
