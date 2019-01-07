node{
    stage('Fetch'){
        git 'https://github.com/CraigDoyle/studentAttendance.git'
    }
    stage('Build'){
        bat '''
        javac -cp "C:\\Program Files (x86)\\JetBrains\\IntelliJ IDEA 2016.3\\lib\\junit-4.12.jar";"C:\\Program Files (x86)\\JetBrains\\IntelliJ IDEA 2016.3\\lib\\hamcrest-core-1.3.jar";. Student.java studentTest.java
        '''
    }
    stage('Test'){
        bat '''
        java -cp "C:\\Program Files (x86)\\JetBrains\\IntelliJ IDEA 2016.3\\lib\\junit-4.12.jar";"C:\\Program Files (x86)\\JetBrains\\IntelliJ IDEA 2016.3\\lib\\hamcrest-core-1.3.jar";. org.junit.runner.JUnitCore studentTest
        '''
    }
}
