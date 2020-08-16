本周着重学习递归，围绕递归引出分治、回溯算法。
递归模板：
public void recur(int level,int param){
	if(level>Max_level){//终结条件
		return;
    }

    process(level,param);//处理当前逻辑

    recur(level+1,newParam);//下探到下一层
}

分治思路：
terminator----->process(split your big problem)----->drill down(subproblems),merge(subresult)----->reverse states。
概括说，将原问题划分成n个规模较小，并且结构与原问题相似的子问题，递归地解决这些子问题，然后再合并其结果，就得到原问题的解。

回溯思想：
将问题求解的过程分为多个阶段。每个阶段都会面对一个岔路口，先随意选一条路走，当发现这条路走不通的时候，就回退到上一个岔路口，另选一种走法继续。回溯算法非常适合用递归来实现，在实现的过程中，剪枝操作是提高回溯效率的一种技巧。