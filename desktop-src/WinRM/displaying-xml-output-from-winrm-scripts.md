---
title: Mostrar la salida XML de los scripts de WinRM
description: Administración remota de Windows scripts devuelven XML en lugar de objetos. El XML no tiene un formato legible. Puede usar los métodos de la API de MSXML y el archivo XSL preinstalado para transformar los datos en un formato legible.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c70dd0a61181f6fc61e685641ff0ed5e3d43ffe8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078145"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="85a5b-105">Mostrar la salida XML de los scripts de WinRM</span><span class="sxs-lookup"><span data-stu-id="85a5b-105">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="85a5b-106">Administración remota de Windows scripts devuelven XML en lugar de objetos.</span><span class="sxs-lookup"><span data-stu-id="85a5b-106">Windows Remote Management scripts return XML rather than objects.</span></span> <span data-ttu-id="85a5b-107">El XML no tiene un formato legible.</span><span class="sxs-lookup"><span data-stu-id="85a5b-107">The XML is not in a human-readable format.</span></span> <span data-ttu-id="85a5b-108">Puede usar los métodos de la API de [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) y el archivo XSL preinstalado para transformar los datos en un formato legible.</span><span class="sxs-lookup"><span data-stu-id="85a5b-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API and the preinstalled XSL file to transform the data into human-readable format.</span></span>

<span data-ttu-id="85a5b-109">Para obtener más información acerca de la salida XML de WinRM y ejemplos de XML y sin formato, vea [Scripting in administración remota de Windows](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="85a5b-109">For more information about WinRM XML output and examples of raw and formatted XML, see [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="85a5b-110">La herramienta de línea de comandos de **WinRM** incluye un archivo de transformación denominado WsmTxt. XSL que muestra la salida en un formato tabular.</span><span class="sxs-lookup"><span data-stu-id="85a5b-110">The **Winrm** command-line tool comes with a transform file named WsmTxt.xsl that displays output in a tabular form.</span></span> <span data-ttu-id="85a5b-111">Si el script suministra este archivo a los métodos MSXML que realizan transforma, la salida aparece igual que la salida de la herramienta **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="85a5b-111">If your script supplies this file to the MSXML methods that perform tranforms, the output appears the same as the output from the **Winrm** tool.</span></span>

<span data-ttu-id="85a5b-112">**Para dar formato a la salida XML sin formato**</span><span class="sxs-lookup"><span data-stu-id="85a5b-112">**To format raw XML output**</span></span>

1.  <span data-ttu-id="85a5b-113">Cree el objeto [**WSMan**](wsman.md) y cree una sesión.</span><span class="sxs-lookup"><span data-stu-id="85a5b-113">Create the [**WSMan**](wsman.md) object and create a session.</span></span>

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  <span data-ttu-id="85a5b-114">Cree objetos MSXML que representen la salida de respuesta XML y la transformación XSL.</span><span class="sxs-lookup"><span data-stu-id="85a5b-114">Create MSXML objects that represent the XML response output and the XSL transform.</span></span>

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  <span data-ttu-id="85a5b-115">Obtener datos a través de métodos de objeto de [**sesión**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="85a5b-115">Obtain data through [**Session**](session.md) object methods.</span></span>

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  <span data-ttu-id="85a5b-116">Proporcione la respuesta al método [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) de MSXML y el método [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) para almacenar el archivo de transformación.</span><span class="sxs-lookup"><span data-stu-id="85a5b-116">Supply the response to the MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) method and the [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) method to store the transform file.</span></span>

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  <span data-ttu-id="85a5b-117">Usar el método [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) de MSXML y mostrar o guardar la salida.</span><span class="sxs-lookup"><span data-stu-id="85a5b-117">Use the MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) method and display or save the output.</span></span>

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

<span data-ttu-id="85a5b-118">En el siguiente ejemplo de código VBScript se muestra el script completo.</span><span class="sxs-lookup"><span data-stu-id="85a5b-118">The following VBScript code example shows the complete script.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set Session = Wsman.CreateSession
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(xmlResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)
```



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a><span data-ttu-id="85a5b-119">Agregar una subrutina portable para transformar XML en los scripts</span><span class="sxs-lookup"><span data-stu-id="85a5b-119">Adding a Portable Subroutine to Transform XML to Your Scripts</span></span>

<span data-ttu-id="85a5b-120">Puede Agregar una subrutina a los scripts que utiliza el archivo XSL preinstalado para convertir la salida XML sin formato de un script WinRM a un formato tabular.</span><span class="sxs-lookup"><span data-stu-id="85a5b-120">You can add a subroutine to your scripts that uses the preinstalled XSL file to convert the raw XML output from a WinRM script to a tabular form.</span></span>

<span data-ttu-id="85a5b-121">La subrutina siguiente usa llamadas a los métodos de scripting de MSXML para proporcionar la salida a WsmTxt. Xsl.</span><span class="sxs-lookup"><span data-stu-id="85a5b-121">The following subroutine uses calls to the MSXML scripting methods to supply the output to WsmTxt.xsl.</span></span>


```VB
'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile)
End Sub
```



<span data-ttu-id="85a5b-122">La subrutina siguiente transforma cada línea de los datos tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="85a5b-122">The following subroutine transforms each line of your data as shown in the following example.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_LogicalDisk"
Set objResultSet = objSession.Enumerate(strResource)
While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub 
```



## <a name="related-topics"></a><span data-ttu-id="85a5b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85a5b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85a5b-124">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="85a5b-124">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="85a5b-125">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="85a5b-125">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="85a5b-126">Referencia de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="85a5b-126">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 