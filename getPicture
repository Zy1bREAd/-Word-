import zipfile
import shutil
import time

def getPicture(doc_path,image_path):
    start_time = time.time()
    doc = zipfile.ZipFile(doc_path)     
    #doc是个ZipFile对象，在创建ZipFile对象时，默认参数是r，表示读已经存在的zip文件，还有w和a，分别为新建和覆盖一个zip文件

    for info in doc.infolist():         #infolist()是获取zip文件中所有文件的信息，返回一个列表
    #print(info.filename.endswith)
        if (info.filename.endswith((".jpeg",".png",".gif"))):       #找到文档中图片并用extract方法解压出来，即提取文档中的图片
            print(info)
            doc.extract(info,image_path)
    doc.close()
    end_time = time.time()
    print(f"总共耗时：{end_time-start_time} 秒")

doc_path = r'J:\09wwq\（人工智能学院）陈俞强12.30(1).docx'      
image_path = r'J:\09wwq\target'
getPicture(doc_path,image_path)
