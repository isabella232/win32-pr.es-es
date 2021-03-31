---
title: Método Session. Invoke (WSManDisp. h)
description: Invoca un método y devuelve los resultados de la llamada al método.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Invocar método Administración remota de Windows
- Método Invoke Administración remota de Windows, objeto Session
- Administración remota de Windows de objeto de sesión, método Invoke
topic_type:
- apiref
api_name:
- Session.Invoke
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117c688b616f377730524a09234b1dc38a4996c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803566"
---
# <a name="sessioninvoke-method"></a><span data-ttu-id="aebd5-106">Session. Invoke (método)</span><span class="sxs-lookup"><span data-stu-id="aebd5-106">Session.Invoke method</span></span>

<span data-ttu-id="aebd5-107">Invoca un método y devuelve los resultados de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="aebd5-107">Invokes a method and returns the results of the method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="aebd5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aebd5-108">Syntax</span></span>


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="aebd5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aebd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aebd5-110">*actionUri* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aebd5-110">*actionUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aebd5-111">URI del método que se va a invocar.</span><span class="sxs-lookup"><span data-stu-id="aebd5-111">The URI of the method to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="aebd5-112">*resourceUri* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aebd5-112">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aebd5-113">Identificador del recurso que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="aebd5-113">The identifier of the resource to retrieve.</span></span>

<span data-ttu-id="aebd5-114">Este parámetro puede contener uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="aebd5-114">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="aebd5-115">URI con o sin [*selectores*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="aebd5-115">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="aebd5-116">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript), la clave se especifica mediante `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="aebd5-116">In the following Visual Basic Scripting Edition (VBScript) example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="aebd5-117">Objeto [**ResourceLocator**](resourcelocator.md) que puede contener selectores, [*fragmentos*](windows-remote-management-glossary.md)u [*Opciones*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="aebd5-117">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="aebd5-118">Referencia del punto de conexión de [*WS-Addressing*](windows-remote-management-glossary.md) como se describe en el estándar [protocolo WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="aebd5-118">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="aebd5-119">Para obtener más información acerca de la especificación pública para el protocolo de WS-Management, consulte la [Página de índice de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="aebd5-119">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="aebd5-120">*parámetros* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="aebd5-120">*parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aebd5-121">Representación XML de la entrada para el método.</span><span class="sxs-lookup"><span data-stu-id="aebd5-121">The XML representation of the input for the method.</span></span> <span data-ttu-id="aebd5-122">Esta cadena se debe proporcionar o se producirá un error en este método.</span><span class="sxs-lookup"><span data-stu-id="aebd5-122">This string must be supplied or this method will fail.</span></span>

</dd> <dt>

<span data-ttu-id="aebd5-123">*marcas* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="aebd5-123">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aebd5-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="aebd5-124">Reserved.</span></span> <span data-ttu-id="aebd5-125">Se debe establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="aebd5-125">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aebd5-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aebd5-126">Return value</span></span>

<span data-ttu-id="aebd5-127">Representación XML de la salida del método.</span><span class="sxs-lookup"><span data-stu-id="aebd5-127">The XML representation of the method output.</span></span>

## <a name="examples"></a><span data-ttu-id="aebd5-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="aebd5-128">Examples</span></span>

<span data-ttu-id="aebd5-129">En el siguiente ejemplo de código de VBScript se inicia un proceso de Calc.exe.</span><span class="sxs-lookup"><span data-stu-id="aebd5-129">The following VBScript code example starts a Calc.exe process.</span></span> <span data-ttu-id="aebd5-130">El parámetro *strInputParameters* contiene los parámetros de entrada en formato XML.</span><span class="sxs-lookup"><span data-stu-id="aebd5-130">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="aebd5-131">El único parámetro de entrada necesario para el método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la clase de [**\_ proceso**](/windows/desktop/CIMWin32Prov/win32-process) de WMI Win32 es la línea de comandos que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="aebd5-131">The only required input parameter for the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is the command line to execute.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

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



<span data-ttu-id="aebd5-132">El siguiente ejemplo de código de VBScript llama al método **Session. Invoke** para ejecutar el método [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="aebd5-132">The following VBScript code example calls the **Session.Invoke** method to execute the [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) method of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="aebd5-133">El método **StopService** no tiene parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="aebd5-133">The **StopService** method does not have input parameters.</span></span> <span data-ttu-id="aebd5-134">Sin embargo, el método **Invoke** requiere una cadena XML en el parámetro *Parameters* .</span><span class="sxs-lookup"><span data-stu-id="aebd5-134">However, the **Invoke** method requires an XML string in the *parameters* parameter.</span></span>


```VB
Option Explicit

Dim objWsman
Dim objSession
Dim strResponse
Dim strActionURI
Dim strInputXml
Dim strResourceURI
Dim strMethodName

set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession
strResourceURI = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=w32time"
strMethodName = "StopService"
strActionURI = strMethodName                                      

strInputXml = "<p:StopService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"

strResponse = objSession.Invoke(strMethodName, strResourceURI, strInputXml)

call DisplayOutput(strResponse)
 
strMethodName = "StartService" 
strActionURI = strResourceURI & "/" & strMethodName  
strInputXml = "<p:StartService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"
strResponse = objSession.Invoke(strMethodName, _
    strResourceURI, strInputXml)

call DisplayOutput(strResponse)

 
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



## <a name="requirements"></a><span data-ttu-id="aebd5-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aebd5-135">Requirements</span></span>



| <span data-ttu-id="aebd5-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="aebd5-136">Requirement</span></span> | <span data-ttu-id="aebd5-137">Value</span><span class="sxs-lookup"><span data-stu-id="aebd5-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aebd5-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aebd5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="aebd5-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aebd5-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="aebd5-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aebd5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="aebd5-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aebd5-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="aebd5-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aebd5-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="aebd5-143"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="aebd5-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="aebd5-144">IDL</span><span class="sxs-lookup"><span data-stu-id="aebd5-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aebd5-145"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aebd5-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="aebd5-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aebd5-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="aebd5-147"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aebd5-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aebd5-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aebd5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aebd5-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aebd5-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aebd5-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="aebd5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aebd5-151">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="aebd5-151">**Session**</span></span>](session.md)
</dt> </dl>

 

