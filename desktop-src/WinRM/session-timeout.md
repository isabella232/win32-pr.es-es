---
title: Propiedad Session. Timeout (WSManDisp. h)
description: Establece y obtiene el tiempo máximo, en milisegundos, que la aplicación cliente espera a que se completen las operaciones de Administración remota de Windows.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Propiedad timeout Administración remota de Windows
- Propiedad timeout Administración remota de Windows, objeto Session
- Objeto de sesión Administración remota de Windows, propiedad timeout
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c28b5284d9061e1c80fb3c66193d394c347a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359870"
---
# <a name="sessiontimeout-property"></a><span data-ttu-id="b79ca-106">Propiedad Session. Timeout</span><span class="sxs-lookup"><span data-stu-id="b79ca-106">Session.Timeout property</span></span>

<span data-ttu-id="b79ca-107">Establece y obtiene el tiempo máximo, en milisegundos, que la aplicación cliente espera a que se completen las operaciones de Administración remota de Windows.</span><span class="sxs-lookup"><span data-stu-id="b79ca-107">Sets and gets the maximum amount of time, in milliseconds, that the client application waits for Windows Remote Management to complete its operations.</span></span>

<span data-ttu-id="b79ca-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b79ca-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79ca-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b79ca-109">Syntax</span></span>


```VB
Session.Timeout As long
```



## <a name="property-value"></a><span data-ttu-id="b79ca-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b79ca-110">Property value</span></span>

<span data-ttu-id="b79ca-111">Valor de tiempo de espera, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b79ca-111">Time-out value, in milliseconds.</span></span> <span data-ttu-id="b79ca-112">Cuando se supera el valor de tiempo de espera, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b79ca-112">When the time-out value is exceeded, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="b79ca-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b79ca-113">Remarks</span></span>

<span data-ttu-id="b79ca-114">El valor de tiempo de espera se puede establecer antes de cada operación realizada por el agente.</span><span class="sxs-lookup"><span data-stu-id="b79ca-114">The time-out value can be set before each operation performed by the agent.</span></span> <span data-ttu-id="b79ca-115">Si no se especifica un valor de tiempo de espera, el agente establece el valor de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="b79ca-115">If a time-out value is not specified, the agent sets the time-out value.</span></span>

<span data-ttu-id="b79ca-116">Durante una operación de enumeración, no se puede restablecer el valor de tiempo de espera mientras se está enumerando el recurso.</span><span class="sxs-lookup"><span data-stu-id="b79ca-116">During an enumerate operation, the time-out value cannot be reset while the resource is being enumerated.</span></span>

## <a name="examples"></a><span data-ttu-id="b79ca-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b79ca-117">Examples</span></span>

<span data-ttu-id="b79ca-118">En el siguiente ejemplo de código de VBScript se inicia un proceso de Calc.exe con el método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la clase de [**\_ proceso WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="b79ca-118">The following VBScript code example starts a Calc.exe process using the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span> <span data-ttu-id="b79ca-119">El parámetro *strInputParameters* contiene los parámetros de entrada en formato XML.</span><span class="sxs-lookup"><span data-stu-id="b79ca-119">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="b79ca-120">El script especifica un tiempo de espera para la sesión.</span><span class="sxs-lookup"><span data-stu-id="b79ca-120">The script specifies a time-out for the session.</span></span>


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

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

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



## <a name="requirements"></a><span data-ttu-id="b79ca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b79ca-121">Requirements</span></span>



| <span data-ttu-id="b79ca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b79ca-122">Requirement</span></span> | <span data-ttu-id="b79ca-123">Value</span><span class="sxs-lookup"><span data-stu-id="b79ca-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b79ca-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b79ca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b79ca-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b79ca-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b79ca-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b79ca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b79ca-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b79ca-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b79ca-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b79ca-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b79ca-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b79ca-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b79ca-130">IDL</span><span class="sxs-lookup"><span data-stu-id="b79ca-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b79ca-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b79ca-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b79ca-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b79ca-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b79ca-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b79ca-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b79ca-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b79ca-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b79ca-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b79ca-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b79ca-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b79ca-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79ca-137">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="b79ca-137">**Session**</span></span>](session.md)
</dt> </dl>

 

