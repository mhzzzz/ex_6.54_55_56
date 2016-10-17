# ex_6.54_55_56
功能可以实现，但是不如pexy的简洁，还是需要注意一些细节问题

    #include<iostream>
    #include<vector>

    using std::cout;
    using std::vector;
    using std::endl;

    using F = int(int, int);

    int fNum(int i, int j)
    {
	    int sum;
	    sum = i + j;
	    return sum;
    } 

    int fSub(int i, int j)
    {
	    int sum;
	    sum = i - j;
	    return sum;
    }

    int fMul(int i, int j)
    {
	    int sum;
	    sum = i * j;
	    return sum;
    }

    int fDiv(int i, int j)
    {
	    int sum;
	    sum = i / j;
	    return sum;
    }

    int main()
    {
	    vector<F*> v{fNum, fSub, fMul, fDiv};

	    for(auto beg = v.begin(); beg != v.end(); ++beg)
	    {
		    cout<<(*beg)(1, 2)<<endl;
	    }
    /*	
        for(auto &rsp : v)	这样写，rsp的类型是从v这继承的，v是个vector类型，输出rsp的波尔值了 
	    cout<<rsp<<endl;
    */
	    return 0;
    }
