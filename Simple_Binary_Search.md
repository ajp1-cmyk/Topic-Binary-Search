## Binary Search

// template to use

int binary_search(vector<int> &a, int query){
  int left = 0;
  int right = a.size()-1;

  while(left < right){
    int mid = left + (right-left)/2;
    if(a[mid] < query){
        left = mid+1;
      }else{
      
      }
  }
}
