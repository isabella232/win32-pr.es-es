---
title: Consultar instancias específicas de un recurso
description: La llamada a Session. Enumerate tiene parámetros opcionales que restringen la enumeración a una consulta.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704963"
---
# <a name="querying-for-specific-instances-of-a-resource"></a><span data-ttu-id="4271a-103">Consultar instancias específicas de un recurso</span><span class="sxs-lookup"><span data-stu-id="4271a-103">Querying for Specific Instances of a Resource</span></span>

<span data-ttu-id="4271a-104">La llamada a [**Session. Enumerate**](session-enumerate.md) tiene parámetros opcionales que restringen la enumeración a una consulta.</span><span class="sxs-lookup"><span data-stu-id="4271a-104">The call to [**Session.Enumerate**](session-enumerate.md) has optional parameters that narrow the enumeration into a query.</span></span> <span data-ttu-id="4271a-105">Dado que la [API de scripting de WinRM](winrm-scripting-api.md) y la API de C++ de [WinRM](winrm-c---api.md) se modelan estrechamente en el protocolo de WS-Management subyacente, los parámetros usan la misma terminología para realizar consultas como el protocolo:*filtrar* y *filtrar el dialecto*.</span><span class="sxs-lookup"><span data-stu-id="4271a-105">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) are closely modeled on the underlying WS-Management protocol, the parameters use the same terminology for querying as the protocol—*filter* and *filter dialect*.</span></span>

<span data-ttu-id="4271a-106">Puede usar los parámetros Filter y Dialect de [**Session. Enumerate**](session-enumerate.md) o puede construir y proporcionar un objeto [**ResourceLocator**](resourcelocator.md) y el método [**AddSelector**](resourcelocator-addselector.md) , pero no puede hacer ambas cosas.</span><span class="sxs-lookup"><span data-stu-id="4271a-106">You can either use the filter and dialect parameters of [**Session.Enumerate**](session-enumerate.md) or you can construct and supply a [**ResourceLocator**](resourcelocator.md) object and the [**AddSelector**](resourcelocator-addselector.md) method, but you cannot do both.</span></span>

<span data-ttu-id="4271a-107">Este procedimiento ejecuta una consulta para los adaptadores de red que tienen TCP/IP enlazado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="4271a-107">This procedure executes a query for network adapters that have TCP/IP bound and enabled.</span></span> <span data-ttu-id="4271a-108">La consulta solicita todas las instancias de [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) que tienen la propiedad **IpEnabled** establecida en **true**.</span><span class="sxs-lookup"><span data-stu-id="4271a-108">The query requests all the instances of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) that have the **IpEnabled** property set to **True**.</span></span> <span data-ttu-id="4271a-109">A excepción de la adición del *filtro* y del *dialecto*, la consulta se trata como una enumeración simple.</span><span class="sxs-lookup"><span data-stu-id="4271a-109">Except for the addition of the *filter* and *dialect*, the query is handled like a simple enumeration.</span></span>

<span data-ttu-id="4271a-110">En este ejemplo, el nombre de recurso para la constante de recurso se representa con un asterisco " \* " porque el nombre de clase, [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), ya se menciona en la cadena *strFilter* .</span><span class="sxs-lookup"><span data-stu-id="4271a-110">In this example, the resource name for the Resource constant is represented by an asterisk "\*" because the class name, [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), is already mentioned in the *strFilter* string.</span></span>

<span data-ttu-id="4271a-111">**Para consultar instancias específicas de un recurso**</span><span class="sxs-lookup"><span data-stu-id="4271a-111">**To query for specific instances of a resource**</span></span>

1.  <span data-ttu-id="4271a-112">Para facilitar la lectura, defina los URI como constantes.</span><span class="sxs-lookup"><span data-stu-id="4271a-112">For ease-of-reading, define URIs as constants.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  <span data-ttu-id="4271a-113">Crear una sesión.</span><span class="sxs-lookup"><span data-stu-id="4271a-113">Create a session.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  <span data-ttu-id="4271a-114">Construya la cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="4271a-114">Construct the filter string.</span></span> <span data-ttu-id="4271a-115">Administración remota de Windows admite [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) como dialecto de filtro.</span><span class="sxs-lookup"><span data-stu-id="4271a-115">Windows Remote Management supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as the filter dialect.</span></span>

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  <span data-ttu-id="4271a-116">Establezca las [**constantes de enumeración**](enumeration-constants.md) necesarias en el parámetro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="4271a-116">Set any required [**enumeration constants**](enumeration-constants.md) in the *flags* parameter.</span></span>

    <span data-ttu-id="4271a-117">Tenga en cuenta que si las marcas incluyen las [**constantes de enumeración**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow** , el servicio WinRM devuelve el error del código de error del **modo de \_ \_ polimorfismo WSMAN \_ \_ no compatible**.</span><span class="sxs-lookup"><span data-stu-id="4271a-117">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then WinRM service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

5.  <span data-ttu-id="4271a-118">Llame al método [**Session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="4271a-118">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="4271a-119">Esta llamada inicia una enumeración.</span><span class="sxs-lookup"><span data-stu-id="4271a-119">This call starts an enumeration.</span></span> <span data-ttu-id="4271a-120">El método **Session. Enumerate** establece un contexto de enumeración de protocolo WS-Management, mantenido en el objeto de [**enumerador**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="4271a-120">The **Session.Enumerate** method establishes a WS-Management protocol enumeration context, maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  <span data-ttu-id="4271a-121">Llame al método [**enumerador. ReadItem**](enumerator-readitem.md) para obtener el siguiente elemento de los resultados.</span><span class="sxs-lookup"><span data-stu-id="4271a-121">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="4271a-122">En WS-Management protocolo, esto corresponde a la operación de extracción.</span><span class="sxs-lookup"><span data-stu-id="4271a-122">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="4271a-123">Use el método [**enumerador. AtEndOfStream**](enumerator-atendofstream.md) como control para saber cuándo detener la lectura.</span><span class="sxs-lookup"><span data-stu-id="4271a-123">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

<span data-ttu-id="4271a-124">En el siguiente ejemplo de código VBScript se muestra el script completo.</span><span class="sxs-lookup"><span data-stu-id="4271a-124">The following VBScript code example shows the complete script.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="4271a-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4271a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4271a-126">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="4271a-126">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="4271a-127">Enumerar o enumerar todas las instancias de un recurso</span><span class="sxs-lookup"><span data-stu-id="4271a-127">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="4271a-128">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="4271a-128">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 