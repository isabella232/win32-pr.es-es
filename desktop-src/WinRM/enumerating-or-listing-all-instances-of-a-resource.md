---
title: Enumerar o enumerar todas las instancias de un recurso
description: El método Session. Enumerate es el Administración remota de Windows enfoque para obtener todas las instancias de un recurso especificado.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54587ce97ec6ed5e87af8b0424a6a18d684f7698
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271322"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a><span data-ttu-id="44c80-103">Enumerar o enumerar todas las instancias de un recurso</span><span class="sxs-lookup"><span data-stu-id="44c80-103">Enumerating or Listing All Instances of a Resource</span></span>

<span data-ttu-id="44c80-104">El método [**Session. Enumerate**](session-enumerate.md) es el administración remota de Windows enfoque para obtener todas las instancias de un recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="44c80-104">The [**Session.Enumerate**](session-enumerate.md) method is the Windows Remote Management approach to obtaining all the instances of a specified resource.</span></span>

<span data-ttu-id="44c80-105">El método [**Session. Enumerate**](session-enumerate.md) no obtiene una colección en un objeto [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) como una llamada a [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) con una [consulta WMI](/windows/desktop/WmiSdk/querying-wmi) como parámetro (por ejemplo, `ExecQuery("SELECT * from Win32_LogicalDisk")` ) o una llamada a un método como [**SWbemObject. instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span><span class="sxs-lookup"><span data-stu-id="44c80-105">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in a [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) object like a [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) call with a [WMI query](/windows/desktop/WmiSdk/querying-wmi) as a parameter (for example, `ExecQuery("SELECT * from Win32_LogicalDisk")`), or a call to a method like [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span> <span data-ttu-id="44c80-106">**Session. Enumerate** y los métodos del objeto de [**enumerador**](enumerator.md) son mucho más similares a la operación del objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de scripting que se usa para leer archivos como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="44c80-106">**Session.Enumerate** and the [**Enumerator**](enumerator.md) object methods are much more similar to the operation of the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object that is used for reading files as a stream.</span></span>

<span data-ttu-id="44c80-107">Para leer archivos como una secuencia de texto, debe crear el objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) scripting y llamar al método [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) para leer cada línea del archivo.</span><span class="sxs-lookup"><span data-stu-id="44c80-107">To read files as a text stream, you must create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="44c80-108">De forma similar, puede llamar al método [**Session. Enumerate**](session-enumerate.md) para obtener un objeto de [**enumerador**](enumerator.md) y llamar al método [**enumerador. ReadItem**](enumerator-readitem.md) para obtener el elemento siguiente.</span><span class="sxs-lookup"><span data-stu-id="44c80-108">In a similar way, you can call the [**Session.Enumerate**](session-enumerate.md) method to obtain an [**Enumerator**](enumerator.md) object and call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to get the next item.</span></span> <span data-ttu-id="44c80-109">Como ocurre cuando se lee desde el archivo de texto, se puede llamar a la propiedad [**enumerador. AtEndOfStream**](enumerator-atendofstream.md) para comprobar si se ha alcanzado el final de los elementos de datos.</span><span class="sxs-lookup"><span data-stu-id="44c80-109">As is the case when reading from the text file, you can call the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

<span data-ttu-id="44c80-110">**Para enumerar un recurso**</span><span class="sxs-lookup"><span data-stu-id="44c80-110">**To enumerate a resource**</span></span>

1.  <span data-ttu-id="44c80-111">Crear una sesión.</span><span class="sxs-lookup"><span data-stu-id="44c80-111">Create a session.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  <span data-ttu-id="44c80-112">Construya el URI para identificar el recurso.</span><span class="sxs-lookup"><span data-stu-id="44c80-112">Construct the URI to identify the resource.</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  <span data-ttu-id="44c80-113">Llame al método [**Session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="44c80-113">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="44c80-114">Esta llamada inicia una enumeración.</span><span class="sxs-lookup"><span data-stu-id="44c80-114">This call starts an enumeration.</span></span> <span data-ttu-id="44c80-115">En WinRM, una operación de enumeración no obtiene una colección del mismo modo que lo hace WMI.</span><span class="sxs-lookup"><span data-stu-id="44c80-115">In WinRM, an enumeration operation does not obtain a collection in the same way that WMI does.</span></span> <span data-ttu-id="44c80-116">En su lugar, el método **Session. Enumerate** establece un contexto de enumeración de protocolo WS-Management que se mantiene en el objeto de [**enumerador**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="44c80-116">Instead, the **Session.Enumerate** method establishes a WS-Management protocol enumeration context that is maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  <span data-ttu-id="44c80-117">Llame al método [**enumerador. ReadItem**](enumerator-readitem.md) para obtener el siguiente elemento de los resultados.</span><span class="sxs-lookup"><span data-stu-id="44c80-117">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="44c80-118">En WS-Management protocolo, esto corresponde a la operación de extracción.</span><span class="sxs-lookup"><span data-stu-id="44c80-118">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="44c80-119">Use el método [**enumerador. AtEndOfStream**](enumerator-atendofstream.md) como control para saber cuándo detener la lectura.</span><span class="sxs-lookup"><span data-stu-id="44c80-119">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

<span data-ttu-id="44c80-120">En el siguiente ejemplo de código VBScript se muestra el script completo.</span><span class="sxs-lookup"><span data-stu-id="44c80-120">The following VBScript code example shows the complete script.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
Wend
Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="44c80-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44c80-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c80-122">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="44c80-122">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="44c80-123">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="44c80-123">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="44c80-124">Referencia de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="44c80-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 