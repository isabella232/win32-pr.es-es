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
# <a name="accessing-services-using-java"></a><span data-ttu-id="485b8-103">Acceso a servicios mediante Java</span><span class="sxs-lookup"><span data-stu-id="485b8-103">Accessing Services Using Java</span></span>

<span data-ttu-id="485b8-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="485b8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="485b8-105">También puede tener acceso a los servicios de Microsoft Agent desde un applet de Java.</span><span class="sxs-lookup"><span data-stu-id="485b8-105">You can also access Microsoft Agent services from a Java applet.</span></span> <span data-ttu-id="485b8-106">Muchas de las funciones a las que se puede tener acceso a través de las interfaces del agente de Microsoft devuelven valores mediante parámetros pasados por referencia.</span><span class="sxs-lookup"><span data-stu-id="485b8-106">Many of the functions accessible through the Microsoft Agent interfaces return values through parameters passed by reference.</span></span> <span data-ttu-id="485b8-107">Para pasar estos parámetros desde Java, es necesario crear matrices de un solo elemento en el código y pasarlas como parámetros a la función adecuada.</span><span class="sxs-lookup"><span data-stu-id="485b8-107">In order to pass these parameters from Java, it is necessary to create single-element arrays in your code and pass them as parameters to the appropriate function.</span></span> <span data-ttu-id="485b8-108">Si usa Microsoft Visual J++ y ha ejecutado el Asistente para la biblioteca de tipos Java en el servidor de agente de Microsoft, consulte el archivo de summary.txt para revisar qué funciones requieren argumentos de matriz.</span><span class="sxs-lookup"><span data-stu-id="485b8-108">If you are using Microsoft Visual J++ and have run the Java Type Library Wizard on the Microsoft Agent server, refer to the summary.txt file to review which functions require array arguments.</span></span> <span data-ttu-id="485b8-109">El procedimiento es similar al de C; la interfaz [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) se usa para crear una instancia del servidor y, a continuación, cargar el carácter:</span><span class="sxs-lookup"><span data-stu-id="485b8-109">The procedure is similar to that in C; you use the [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) interface to create an instance of the server, then load the character:</span></span>


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



<span data-ttu-id="485b8-110">El procedimiento es ligeramente diferente cuando se cargan caracteres de una ubicación remota HTTP como, por ejemplo, un sitio Web.</span><span class="sxs-lookup"><span data-stu-id="485b8-110">The procedure is slightly different when loading characters from a HTTP remote location such as a website.</span></span> <span data-ttu-id="485b8-111">En este caso, el método [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) es asincrónico y generará una excepción com de E \_ pendiente (0x8000000a).</span><span class="sxs-lookup"><span data-stu-id="485b8-111">In this case the [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) method is asynchronous and will raise a COM exception of E\_PENDING (0x8000000a).</span></span> <span data-ttu-id="485b8-112">Tendrá que detectar esta excepción y controlarla correctamente tal y como se hace en las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="485b8-112">You will need to catch this exception and handle it correctly as is done in the following functions:</span></span>


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



<span data-ttu-id="485b8-113">A continuación, obtenga la interfaz [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) que le permite tener acceso a sus métodos:</span><span class="sxs-lookup"><span data-stu-id="485b8-113">Then get the [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) interface that enables you to access its methods:</span></span>


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



<span data-ttu-id="485b8-114">Del mismo modo, para recibir notificaciones de eventos, debe implementar la interfaz [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) o [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) , y crear y registrar un objeto de ese tipo:</span><span class="sxs-lookup"><span data-stu-id="485b8-114">Similarly, to be notified of events, you must implement either the [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) or the [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) interface, creating and registering an object of that type:</span></span>


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



<span data-ttu-id="485b8-115">Para tener acceso a Microsoft Agent desde un applet de Java, debe generar las clases de Java que se instalan con el applet.</span><span class="sxs-lookup"><span data-stu-id="485b8-115">In order to access Microsoft Agent from a Java applet, you must generate Java classes that you install with the applet.</span></span> <span data-ttu-id="485b8-116">Puede usar el Asistente para la biblioteca de tipos de Java de Visual J++, por ejemplo, para generar estos archivos.</span><span class="sxs-lookup"><span data-stu-id="485b8-116">You can use the Visual J++ Java Type Library Wizard, for example, to generate these files.</span></span> <span data-ttu-id="485b8-117">Si tiene previsto hospedar el applet en una página web, deberá crear un archivo CAB de Java firmado, incluidos los archivos de clase generados que se descargan con la página.</span><span class="sxs-lookup"><span data-stu-id="485b8-117">If you plan to host the applet on a webpage, you will need to build a signed Java CAB inclusive of the generated class files that download with the page.</span></span> <span data-ttu-id="485b8-118">Los archivos de clase son necesarios para tener acceso al servidor de agente de Microsoft, ya que es un objeto COM, que se ejecuta fuera del espacio aislado de Java.</span><span class="sxs-lookup"><span data-stu-id="485b8-118">The class files are necessary to access the Microsoft Agent Server since it is a COM object, that executes outside of the Java sandbox.</span></span> <span data-ttu-id="485b8-119">Para obtener más información acerca de la seguridad de Trust-Based para Java, vea <https://www.microsoft.com/java/security> .</span><span class="sxs-lookup"><span data-stu-id="485b8-119">To learn more about Trust-Based Security for Java, see <https://www.microsoft.com/java/security>.</span></span>

 

 