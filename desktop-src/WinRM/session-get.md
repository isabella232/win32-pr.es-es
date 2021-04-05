---
title: Método Session. get (WSManDisp. h)
description: Recupera el recurso especificado por el URI y devuelve una representación XML de la instancia actual del recurso.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Método get Administración remota de Windows
- Método get Administración remota de Windows, objeto Session
- Administración remota de Windows de objeto de sesión, get (método)
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4ee84cc711db312389151d1dd95fb890474dcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359802"
---
# <a name="sessionget-method"></a><span data-ttu-id="c1362-106">Session. get (método)</span><span class="sxs-lookup"><span data-stu-id="c1362-106">Session.Get method</span></span>

<span data-ttu-id="c1362-107">Recupera el recurso especificado por el [*URI*](windows-remote-management-glossary.md) y devuelve una representación XML de la instancia actual del recurso.</span><span class="sxs-lookup"><span data-stu-id="c1362-107">Retrieves the resource specified by the [*URI*](windows-remote-management-glossary.md) and returns an XML representation of the current instance of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1362-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1362-108">Syntax</span></span>


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c1362-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1362-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1362-110">*resourceUri* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1362-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1362-111">Identificador del recurso que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c1362-111">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="c1362-112">Este parámetro puede contener uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c1362-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="c1362-113">Un URI con o sin [*selectores*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c1362-113">A URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="c1362-114">Al llamar al método **Get** con un selector para obtener un recurso WMI, utilice la propiedad o propiedades de clave del objeto.</span><span class="sxs-lookup"><span data-stu-id="c1362-114">When calling the **Get** method with a selector to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="c1362-115">Por ejemplo, en el siguiente ejemplo de código de Visual Basic Scripting Edition (VBScript), la clave se especifica mediante `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="c1362-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span> <span data-ttu-id="c1362-116">En el caso de las clases singleton, como [**\_ localtime de Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), no se puede utilizar un selector.</span><span class="sxs-lookup"><span data-stu-id="c1362-116">For singleton classes, such as [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), you cannot use a selector.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   <span data-ttu-id="c1362-117">Un objeto [**ResourceLocator**](resourcelocator.md) que puede contener selectores, [*fragmentos*](windows-remote-management-glossary.md)u [*Opciones*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c1362-117">A [**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="c1362-118">Una referencia de extremo de [*WS-Addressing*](windows-remote-management-glossary.md) como se describe en el estándar del protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="c1362-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="c1362-119">Para obtener más información sobre la especificación pública de [protocolo WS-Management](ws-management-protocol.md), consulte la [Página de índice de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="c1362-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="c1362-120">*marcas* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c1362-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1362-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c1362-121">Reserved.</span></span> <span data-ttu-id="c1362-122">Se debe establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="c1362-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1362-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1362-123">Return value</span></span>

<span data-ttu-id="c1362-124">Representación XML del recurso.</span><span class="sxs-lookup"><span data-stu-id="c1362-124">An XML representation of the resource.</span></span>

## <a name="examples"></a><span data-ttu-id="c1362-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c1362-125">Examples</span></span>

<span data-ttu-id="c1362-126">En el siguiente ejemplo de código de VBScript se recupera la representación XML de la instancia de [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service) que representa el servicio WMI WinMgmt en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="c1362-126">The following VBScript code example retrieves the XML representation of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) instance that represents the WMI Winmgmt service on the local computer.</span></span>


```VB

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub

```



<span data-ttu-id="c1362-127">El siguiente ejemplo de código de VBScript recupera la instancia de servicio de WMI WinMgmt de un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="c1362-127">The following VBScript code example retrieves the WMI Winmgmt service instance from a remote computer.</span></span> <span data-ttu-id="c1362-128">El equipo remoto se identifica mediante el nombre de dominio completo (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="c1362-128">The remote computer is identified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="c1362-129">La única diferencia entre la versión local y la remota es la especificación del equipo remoto en la llamada a [**WSMan. createSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="c1362-129">The only difference between the local and remote version is the specification of the remote computer in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c1362-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1362-130">Requirements</span></span>



| <span data-ttu-id="c1362-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1362-131">Requirement</span></span> | <span data-ttu-id="c1362-132">Value</span><span class="sxs-lookup"><span data-stu-id="c1362-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1362-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1362-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c1362-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1362-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c1362-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1362-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c1362-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1362-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c1362-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1362-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1362-138"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1362-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1362-139">IDL</span><span class="sxs-lookup"><span data-stu-id="c1362-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c1362-140"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c1362-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c1362-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1362-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1362-142"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1362-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1362-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c1362-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1362-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1362-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1362-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1362-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1362-146">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="c1362-146">**Session**</span></span>](session.md)
</dt> </dl>

 

