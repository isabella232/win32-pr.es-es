---
title: Acceso a servicios mediante Java
description: Acceso a servicios mediante Java
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a9a3feb1e6cb5fc9ddb8a24b87adfdb42461ebb4581723c1cdb465739c51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976855"
---
# <a name="accessing-services-using-java"></a>Acceso a servicios mediante Java

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

También puede acceder a los servicios de Microsoft Agent desde un applet de Java. Muchas de las funciones a las que se puede acceder a través de las interfaces de Microsoft Agent devuelven valores a través de parámetros pasados por referencia. Para pasar estos parámetros desde Java, es necesario crear matrices de un solo elemento en el código y pasarlos como parámetros a la función adecuada. Si usa Microsoft Visual J++ y ha ejecutado el Asistente para biblioteca de tipos de Java en el servidor de Microsoft Agent, consulte el archivo summary.txt para revisar qué funciones requieren argumentos de matriz. El procedimiento es similar al de C; use la [**interfaz IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) para crear una instancia del servidor y, a continuación, cargue el carácter:


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



El procedimiento es ligeramente diferente al cargar caracteres desde una ubicación remota HTTP, como un sitio web. En este caso, [**el método Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) es asincrónico y producirá una excepción COM de E PENDING \_ (0x8000000a). Tendrá que detectar esta excepción y controlarla correctamente como se hace en las siguientes funciones:


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



A continuación, [**obtenga la interfaz IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) que le permite acceder a sus métodos:


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



Del mismo modo, para recibir notificaciones de eventos, debe implementar la interfaz [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) o [**IAgentNotifySinkEx,**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) creando y registrando un objeto de ese tipo:


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



Para acceder a Microsoft Agent desde un applet de Java, debe generar clases de Java que instale con el applet. Puede usar el Asistente para biblioteca de tipos java de Visual J++, por ejemplo, para generar estos archivos. Si tiene previsto hospedar el applet en una página web, deberá crear un CAB de Java firmado, incluidos los archivos de clase generados que se descargan con la página. Los archivos de clase son necesarios para tener acceso al servidor de Microsoft Agent, ya que es un objeto COM, que se ejecuta fuera del espacio aislado de Java. Para obtener más información sobre Trust-Based Security for Java, consulte <https://www.microsoft.com/java/security> .

 

 