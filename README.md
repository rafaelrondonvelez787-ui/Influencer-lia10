import time
import webbrowser
while True:
    respuesta_user_name = input (" Nombre de usuario:")
    respuesta_user_name = respuesta_user_name.lower()
    if respuesta_user_name == "la lisa":
       print("correcto")
       while True:
           respuesta_clave = input ("contraseńa:")
           respuesta_clave = respuesta_clave.lower()
           if respuesta_clave == "blackpink":
              print("correcto")
              respuesta_confi=input("\nLia thais la super influencer? si/no")
              if respuesta_confi== "si":
                 print("\n\nMuy bn\n")
                 
              elif respuesta_confi=="no":
                 print("\n\n(Claro que lo eres, pon que si)\n")
              while True:
                 respuesta_confi=input("\nLia thais la super influencer? si/no")
                 if respuesta_confi =="si":
                    print("\n\nMuy bn\n")
                    time.sleep(2)
                    webbrowser.open("https://youtube.com/@andreagonzales-oj2je?si=YrxPfNwthAPFcY1x")
                 elif respuesta_confi=="no":
                      print("\n\n(Claro que lo eres, por que si)\n")
                 
           else:
                print("incorrecto")
       break
    else:
         print("incorrecto")
    
         
         
   
         
         
     
           
       
    
        
        
        