---
title: Método Session. put (WSManDisp. h)
description: Actualiza un recurso.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Método put Administración remota de Windows
- Método put Administración remota de Windows, objeto Session
- Administración remota de Windows de objeto de sesión, Put (método)
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0f09b0a0f8de4e7f7d06cb84753e6b708841f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422458"
---
# <a name="sessionput-method"></a><span data-ttu-id="c7ccb-106">Session. put (método)</span><span class="sxs-lookup"><span data-stu-id="c7ccb-106">Session.Put method</span></span>

<span data-ttu-id="c7ccb-107">Actualiza un recurso.</span><span class="sxs-lookup"><span data-stu-id="c7ccb-107">Updates a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ccb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7ccb-108">Syntax</span></span>


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c7ccb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7ccb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7ccb-110">*resourceUri* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7ccb-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ccb-111">Identificador del recurso que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="c7ccb-111">The identifier of the resource to be updated.</span></span>

<span data-ttu-id="c7ccb-112">Este parámetro puede contener uno de los elementos incluidos en la lista siguiente:</span><span class="sxs-lookup"><span data-stu-id="c7ccb-112">This parameter can contain one of elements contained in the following list:</span></span>

-   <span data-ttu-id="c7ccb-113">URI con o sin [*selectores*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c7ccb-113">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="c7ccb-114">Al llamar al método **Put** para obtener un recurso WMI, utilice la propiedad o propiedades de clave del objeto.</span><span class="sxs-lookup"><span data-stu-id="c7ccb-114">When calling the **Put** method to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="c7ccb-115">Por ejemplo, en el siguiente ejemplo de código de Visual Basic Scripting Edition (VBScript), la clave se especifica mediante `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="c7ccb-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="c7ccb-116">Objeto [**ResourceLocator**](resourcelocator.md) que puede contener selectores, [*fragmentos*](windows-remote-management-glossary.md)u [*Opciones*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c7ccb-116">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="c7ccb-117">Referencia del punto de conexión de [*WS-Addressing*](windows-remote-management-glossary.md) como se describe en el estándar [protocolo WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="c7ccb-117">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="c7ccb-118">Para obtener más información acerca de la especificación pública para el protocolo de WS-Management, consulte la [Página de índice de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="c7ccb-118">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="c7ccb-119">*recurso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c7ccb-119">*resource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ccb-120">El contenido del recurso actualizado.</span><span class="sxs-lookup"><span data-stu-id="c7ccb-120">The updated resource content.</span></span>

</dd> <dt>

<span data-ttu-id="c7ccb-121">*marcas* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c7ccb-121">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ccb-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c7ccb-122">Reserved.</span></span> <span data-ttu-id="c7ccb-123">Se debe establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="c7ccb-123">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7ccb-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7ccb-124">Return value</span></span>

<span data-ttu-id="c7ccb-125">El XML que contiene el contenido del recurso actualizado.</span><span class="sxs-lookup"><span data-stu-id="c7ccb-125">The XML that contains the updated resource content.</span></span>

## <a name="examples"></a><span data-ttu-id="c7ccb-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c7ccb-126">Examples</span></span>

<span data-ttu-id="c7ccb-127">El siguiente ejemplo de código de VBScript escribe datos en el objeto [**\_ WMISetting de Win32**](/windows/desktop/CIMWin32Prov/win32-wmisetting) .</span><span class="sxs-lookup"><span data-stu-id="c7ccb-127">The following VBScript code example writes data to the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) object.</span></span> <span data-ttu-id="c7ccb-128">Debe incluir todas las propiedades que no sean de matriz del objeto en el XML del parámetro de *recurso* .</span><span class="sxs-lookup"><span data-stu-id="c7ccb-128">You must include all non-array properties of the object in the XML of the *Resource* parameter.</span></span> <span data-ttu-id="c7ccb-129">El orden de las propiedades no es significativo.</span><span class="sxs-lookup"><span data-stu-id="c7ccb-129">The order of the properties is not significant.</span></span>


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

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
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



## <a name="requirements"></a><span data-ttu-id="c7ccb-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7ccb-130">Requirements</span></span>



| <span data-ttu-id="c7ccb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7ccb-131">Requirement</span></span> | <span data-ttu-id="c7ccb-132">Value</span><span class="sxs-lookup"><span data-stu-id="c7ccb-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ccb-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7ccb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c7ccb-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7ccb-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c7ccb-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7ccb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c7ccb-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7ccb-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c7ccb-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7ccb-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7ccb-138"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7ccb-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7ccb-139">IDL</span><span class="sxs-lookup"><span data-stu-id="c7ccb-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7ccb-140"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7ccb-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7ccb-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7ccb-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7ccb-142"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7ccb-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7ccb-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7ccb-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7ccb-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7ccb-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7ccb-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7ccb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ccb-146">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="c7ccb-146">**Session**</span></span>](session.md)
</dt> </dl>

 

