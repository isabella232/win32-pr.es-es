---
title: Objeto Enumerator (WSManDisp. h)
description: Representa una secuencia de resultados devuelta de operaciones, como una operación de extracción.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- Objeto enumerador Administración remota de Windows
- Objeto de enumerador Administración remota de Windows, descrito
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079690"
---
# <a name="enumerator-object"></a><span data-ttu-id="150be-105">Enumerator (objeto)</span><span class="sxs-lookup"><span data-stu-id="150be-105">Enumerator object</span></span>

<span data-ttu-id="150be-106">Representa una secuencia de resultados devuelta de operaciones, como una operación de extracción.</span><span class="sxs-lookup"><span data-stu-id="150be-106">Represents a stream of results returned from operations, such as a Pull operation.</span></span> <span data-ttu-id="150be-107">Por ejemplo, el método [**Session. Enumerate**](session-enumerate.md) devuelve varios resultados.</span><span class="sxs-lookup"><span data-stu-id="150be-107">For example, the [**Session.Enumerate**](session-enumerate.md) method returns multiple results.</span></span>

## <a name="members"></a><span data-ttu-id="150be-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="150be-108">Members</span></span>

<span data-ttu-id="150be-109">El objeto de **enumerador** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="150be-109">The **Enumerator** object has these types of members:</span></span>

-   [<span data-ttu-id="150be-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="150be-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="150be-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="150be-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="150be-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="150be-112">Methods</span></span>

<span data-ttu-id="150be-113">El objeto de **enumerador** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="150be-113">The **Enumerator** object has these methods.</span></span>



| <span data-ttu-id="150be-114">Método</span><span class="sxs-lookup"><span data-stu-id="150be-114">Method</span></span>                                  | <span data-ttu-id="150be-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="150be-115">Description</span></span>                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="150be-116">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="150be-116">**ReadItem**</span></span>](enumerator-readitem.md) | <span data-ttu-id="150be-117">Recupera un elemento del recurso y devuelve una representación XML del elemento.</span><span class="sxs-lookup"><span data-stu-id="150be-117">Retrieves an item from the resource and returns an XML representation of the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="150be-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="150be-118">Properties</span></span>

<span data-ttu-id="150be-119">El objeto de **enumerador** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="150be-119">The **Enumerator** object has these properties.</span></span>



| <span data-ttu-id="150be-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="150be-120">Property</span></span>                                                     | <span data-ttu-id="150be-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="150be-121">Description</span></span>                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="150be-122">**AtEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="150be-122">**AtEndOfStream**</span></span>](enumerator-atendofstream.md)<br/> | <span data-ttu-id="150be-123">Obtiene un valor booleano que indica si hay más elementos en la colección.</span><span class="sxs-lookup"><span data-stu-id="150be-123">Gets a Boolean value that indicates whether there are more items in the collection.</span></span><br/> |
| [<span data-ttu-id="150be-124">**Error**</span><span class="sxs-lookup"><span data-stu-id="150be-124">**Error**</span></span>](enumerator-error.md)<br/>                 | <span data-ttu-id="150be-125">Obtiene una representación XML de información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="150be-125">Gets an XML representation of additional error information.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="150be-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="150be-126">Remarks</span></span>

<span data-ttu-id="150be-127">Para iniciar una enumeración, use [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="150be-127">To start an enumeration, use [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="150be-128">Para realizar una operación [*WS-Enumeration:*](windows-remote-management-glossary.md)[*pull*](windows-remote-management-glossary.md) que continúe leyendo los elementos de la enumeración, use [**Enumerator. ReadItem**](enumerator-readitem.md).</span><span class="sxs-lookup"><span data-stu-id="150be-128">To do a [*WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) operation that continues reading items in the enumeration, use [**Enumerator.ReadItem**](enumerator-readitem.md).</span></span>

<span data-ttu-id="150be-129">El objeto de **enumerador** corresponde a la interfaz [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) .</span><span class="sxs-lookup"><span data-stu-id="150be-129">The **Enumerator** object corresponds to the [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="150be-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="150be-130">Examples</span></span>

<span data-ttu-id="150be-131">En el siguiente ejemplo de código de VBScript se enumeran todos los discos de un equipo remoto especificado por el nombre de dominio completo (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="150be-131">The following VBScript code example enumerates all the disks on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="150be-132">La subrutina DisplayOutput da formato a la salida de datos de la misma manera que la herramienta WinRM. cmd.</span><span class="sxs-lookup"><span data-stu-id="150be-132">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


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



## <a name="requirements"></a><span data-ttu-id="150be-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="150be-133">Requirements</span></span>



| <span data-ttu-id="150be-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="150be-134">Requirement</span></span> | <span data-ttu-id="150be-135">Value</span><span class="sxs-lookup"><span data-stu-id="150be-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="150be-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="150be-136">Minimum supported client</span></span><br/> | <span data-ttu-id="150be-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="150be-137">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="150be-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="150be-138">Minimum supported server</span></span><br/> | <span data-ttu-id="150be-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="150be-139">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="150be-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="150be-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="150be-141"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="150be-141"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="150be-142">IDL</span><span class="sxs-lookup"><span data-stu-id="150be-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="150be-143"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="150be-143"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="150be-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="150be-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="150be-145"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="150be-145"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="150be-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="150be-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="150be-147"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="150be-147"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="150be-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="150be-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="150be-149">API de scripting de WinRM</span><span class="sxs-lookup"><span data-stu-id="150be-149">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="150be-150">Enumerar o enumerar todas las instancias de un recurso</span><span class="sxs-lookup"><span data-stu-id="150be-150">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="150be-151">Scripting en Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="150be-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





