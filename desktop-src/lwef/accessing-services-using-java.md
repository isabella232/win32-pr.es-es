---
title: Acceso a servicios mediante Java
description: Acceso a servicios mediante Java
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c24ae7508b5999e5d07f2480d49cb4c20dd89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995161"
---
# <a name="accessing-services-using-java"></a>Acceso a servicios mediante Java

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

También puede tener acceso a los servicios de Microsoft Agent desde un applet de Java. Muchas de las funciones a las que se puede tener acceso a través de las interfaces del agente de Microsoft devuelven valores mediante parámetros pasados por referencia. Para pasar estos parámetros desde Java, es necesario crear matrices de un solo elemento en el código y pasarlas como parámetros a la función adecuada. Si usa Microsoft Visual J++ y ha ejecutado el Asistente para la biblioteca de tipos Java en el servidor de agente de Microsoft, consulte el archivo de summary.txt para revisar qué funciones requieren argumentos de matriz. El procedimiento es similar al de C; la interfaz [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) se usa para crear una instancia del servidor y, a continuación, cargar el carácter:


```
private IAgentEx            m_AgentEx = null;
private IAgentCharacterEx   m_Merlin[] = {null};
private int                 m_MerlinID[] = {-1};
private int                 m_RequestID[] = {0};
private final String        m_CharacterPath = "merlin.acs";

public void start()
{
      // Start the Microsoft Agent Server

      m_AgentEx = (IAgentEx) new AgentServer();

      try
      {

         Variant characterPath = new Variant();
         characterPath.putString(m_CharacterPath);

         // Load the character

         m_AgentEx.Load(characterPath,
                    m_MerlinID,
                    m_RequestID);
      }
```



El procedimiento es ligeramente diferente cuando se cargan caracteres de una ubicación remota HTTP como, por ejemplo, un sitio Web. En este caso, el método [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) es asincrónico y generará una excepción com de E \_ pendiente (0x8000000a). Tendrá que detectar esta excepción y controlarla correctamente tal y como se hace en las siguientes funciones:


```
// Constants used in asynchronous character loads

private final int E_PENDING = 0x8000000a;
private final int NOERROR = 0;


// This function loads a character from the specified path.
// It correctly handles the loading of characters from
// remote sites.

// This sample doesn't care about the request id returned
// from the Load call.  Real production code might use the
// request id and the RequestComplete callback to check for
// a successful character load before proceeding.

public int LoadCharacter(Variant path, int[] id)
{
   int requestid[] = {-1};
   int hRes = 0;

   try
   {
      // Load the character

      m_AgentEx.Load(path, id, requestid);
   }
   catch(com.ms.com.ComException e)
   {
      // Get the HRESULT

      hRes = e.getHResult();
      
      // If the error code is E_PENDING, we return NOERROR

      if (hRes == E_PENDING)
         hRes = NOERROR;
   }

   return hRes;
}

public void start()
{
   if (LoadCharacter(characterPath, m_MerlinID) != NOERROR)
   {
      stop();
      return;
   }

   // Other initialization code here

   .
   .
   .
}
```



A continuación, obtenga la interfaz [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) que le permite tener acceso a sus métodos:


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



Del mismo modo, para recibir notificaciones de eventos, debe implementar la interfaz [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) o [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) , y crear y registrar un objeto de ese tipo:


```
...
// Declare an Agent Notify Sink so that we can get
// notification callbacks from the Agent server.

private AgentNotifySinkEx m_SinkEx = null;
private int            m_SinkID[] = {-1};

public void start()
   {
   ...
   // Create and register a notify sink

   m_SinkEx = new AgentNotifySinkEx();

   m_AgentEx.Register(m_SinkEx, m_SinkID);
   …
   // Give our notify sink access to the character

   m_SinkEx.SetCharacter(m_Merlin[0]);
   ...
   }
```



Para tener acceso a Microsoft Agent desde un applet de Java, debe generar las clases de Java que se instalan con el applet. Puede usar el Asistente para la biblioteca de tipos de Java de Visual J++, por ejemplo, para generar estos archivos. Si tiene previsto hospedar el applet en una página web, deberá crear un archivo CAB de Java firmado, incluidos los archivos de clase generados que se descargan con la página. Los archivos de clase son necesarios para tener acceso al servidor de agente de Microsoft, ya que es un objeto COM, que se ejecuta fuera del espacio aislado de Java. Para obtener más información acerca de la seguridad de Trust-Based para Java, vea <https://www.microsoft.com/java/security> .

 

 