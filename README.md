# test1
package map;

public class Test3 {

	public String findStr(String a){
		if(a==null){
			 return null;
			 }
		int max=0;
		int first=0;
		String res = null;
		for(int i=1;i<a.length();i++){
			for(int k=0,j=0;j<a.length()-i;j++){
				if(a.charAt(j)==a.charAt(j+i)){
					 k++;
					 }
				else{k=0;}
				if(k>max){
					 max=k;
					 first=j-max+1;
				}
				if(max>0){
					res = a.substring(first, first+max);
				}
				}
					
			}
		 return res;
		}
	
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		 String a = "abcddabc";
		 String b = "abcd cc abcd";
		 String c = "abcdf cabdc abcdf";
		 String d = "abcdxyz123cabdcabcd";
		 String e = "abcdadeatde123cabdcabcdadawdawfwaww";
		 System.out.println(new Test3().findStr(a).length());
		 System.out.println(new Test3().findStr(b).length());
		 System.out.println(new Test3().findStr(c).length());
		 System.out.println(new Test3().findStr(d).length());
		 System.out.println(new Test3().findStr(e).length());
		 
	}

}
