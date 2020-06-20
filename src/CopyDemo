package day05;


import java.io.*;

public class CopyDemo {
    public static void main(String[] args) throws FileNotFoundException {
        //创建文件
        File file = new File("src/day05/java.txt");
        File file1 = new File("src/day05/good.txt");
        //读取并写入文件
        Reader reader = null;
        Writer writer = null;
        try {
            reader = new FileReader(file);
            writer = new FileWriter(file1);
            char[] cs = new char[1024];
            int len = -1;
            while ((len = reader.read(cs))!= -1){
                writer.write(cs,0,len);
            }
            writer.flush();
        }catch (IOException e){
            e.printStackTrace();
        }finally {
            try {
                if (writer != null){
                    writer.close();
                }
                if (reader != null){
                    reader.close();
                }
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}
