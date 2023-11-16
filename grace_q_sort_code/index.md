# Grace q_sort Code


### 
public void q_sort(int l,int r, int[] nums){
        if (l >= r) return;
        int i = l - 1;
        int j = r + 1; 
        int x = nums[l + r >> 1];
        while (i < j){
            do i ++ ; while (nums[i] < x);
            do j -- ; while (nums[j] > x);
            if (i < j) {
                int temp = nums[i];
                nums[i] = nums[j];
                nums[j] = temp;
            }
        }
        q_sort(l, j,nums);
        q_sort(j + 1, r,nums);
}

