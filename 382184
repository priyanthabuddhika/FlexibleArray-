class FlexibleArray{
	
	int nElmns = 0; // the number of elements in the array
	int[] mArray; // int array 

	FlexibleArray(int size){
		this.mArray = new int[size]; // initiallizing the array with given size
	}

// Main method 
	public static void main(String[] args) {

		FlexibleArray test = new FlexibleArray(5);  // creates a FlexibleArray object
		test.add(5);
		test.add(7);
		test.add(88);
		test.printArray();
		test.delete(1);
		test.printArray();
		test.update(10,0);
		test.add(6);
		test.add(9);
		test.add(33);
		test.printArray();
		test.deleteS(5);
		test.printArray();
		test.add(34);
		test.add(346);
		test.printArray();	
		
	}
// print method that prints array elements

	public void printArray(){
		for (int i=0; i< nElmns ; i++) {
			System.out.println(""+mArray[i]);
		}
	}
// if array size is full this method will increase array size by 1

	public static int[] changeSize(int[] arr){
		int[] array = new int[arr.length+1];
		for (int i=0;i<arr.length ; i++ ) {
			array[i] = arr[i];
		}
		return array;
	}

// add method ( user can add values to the array )

	public void add (int input){
		if(mArray.length != nElmns ){  // check whether array is full or not 
			this.mArray[nElmns] = input;
			System.out.println(""+input+" added successfully to the array !");
			nElmns++;
		}
		else{
			// 
			mArray = changeSize(mArray);
			this.add(input);
		}
	}

// Delete method which deletes the data at given index

	public void delete(int index){
		if (nElmns !=0 ) {
		// check whether array has at least one element
			if(index<nElmns)
		 	{
				for (int i=index; i < nElmns ; i++ ) {

					this.mArray[i] = this.mArray[i+1];
				}
				System.out.println("value deleted successfully at index "+index);
				nElmns--;  
				}
				// decrement number of element count of array
			else 
				System.out.println("Index is out of bound ! ");
		}
		 else
		 	System.out.println("Array doesn't contain any data !");
	}

// Delete method which deletes array data by searching given value 

	public void deleteS(int value) {
		int i;
		if (nElmns != 0) { 
		// check whether array has at least one element
			for (i = 0; i<nElmns ; i++ ) {
				if (mArray[i] == value){
					for (int j=i; j<nElmns ; j++ ) {
						this.mArray[j] = this.mArray[j+1];
							}
							nElmns--; // decrement element count of array
						}
				else if (i == nElmns-1 ) 
					System.out.println("Can't Find "+value);
				}
				
			}
			 
		else
		 	System.out.println("Array doesn't contain any data !");
	}

// Update method that ovewrite the data at given index
	
	public void update(int value,int index){
		if (index < mArray.length ) {  // check whether given index is within the size of array
			this.mArray[index] = value;
			System.out.println(""+value+" added successfully to the index "+index);
		}
		else
			System.out.println("Given index is out of bound !");
	}
}

