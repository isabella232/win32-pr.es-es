---
title: Propiedad Enumerator. AtEndOfStream (WSManDisp. h)
description: Obtiene un valor booleano que indica si hay más elementos en la colección.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de la propiedad AtEndOfStream
- Propiedad AtEndOfStream Administración remota de Windows, objeto Enumerator
- Objeto enumerador Administración remota de Windows, propiedad AtEndOfStream
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023798f6c868e434218dd1a4dbdf1928bf4526a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150086"
---
# <a name="enumeratoratendofstream-property"></a><span data-ttu-id="e3bd6-106">Enumerador. AtEndOfStream (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e3bd6-106">Enumerator.AtEndOfStream property</span></span>

<span data-ttu-id="e3bd6-107">Obtiene un valor booleano que indica si hay más elementos en la colección.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-107">Gets a Boolean value that indicates whether there are any more items in the collection.</span></span>

<span data-ttu-id="e3bd6-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3bd6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3bd6-109">Syntax</span></span>


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="e3bd6-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e3bd6-110">Property value</span></span>

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="e3bd6-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Reales**</span><span class="sxs-lookup"><span data-stu-id="e3bd6-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</span></span>


</dt> <dd>

<span data-ttu-id="e3bd6-112">No hay más elementos en la colección.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-112">No more items are in the collection.</span></span>

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="e3bd6-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Es**</span><span class="sxs-lookup"><span data-stu-id="e3bd6-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</span></span>


</dt> <dd>

<span data-ttu-id="e3bd6-114">Hay más elementos disponibles.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-114">More items are available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3bd6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3bd6-115">Remarks</span></span>

<span data-ttu-id="e3bd6-116">Si libera el objeto de [**enumerador**](enumerator.md) después de haber obtenido todos los datos necesarios, se quitarán todas las solicitudes de enumeración pendientes.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-116">If you free the [**Enumerator**](enumerator.md) object after you have obtained all the data required, then any pending enumeration requests are removed.</span></span> <span data-ttu-id="e3bd6-117">Para obtener más información, consulte [enumeración o enumeración de todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="e3bd6-117">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e3bd6-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e3bd6-118">Examples</span></span>

<span data-ttu-id="e3bd6-119">En el siguiente ejemplo de VBScript se enumeran las instancias del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-119">The following VBScript example enumerates operating system instances.</span></span> <span data-ttu-id="e3bd6-120">Tenga en cuenta que la liberación del objeto de enumeración limpia todas las solicitudes de enumeración pendientes.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-120">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span> <span data-ttu-id="e3bd6-121">La subrutina DisplayOutput da formato a la salida de datos de la misma manera que la herramienta WinRM. cmd.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-121">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

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



## <a name="requirements"></a><span data-ttu-id="e3bd6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3bd6-122">Requirements</span></span>



| <span data-ttu-id="e3bd6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3bd6-123">Requirement</span></span> | <span data-ttu-id="e3bd6-124">Value</span><span class="sxs-lookup"><span data-stu-id="e3bd6-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3bd6-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3bd6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e3bd6-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3bd6-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e3bd6-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3bd6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e3bd6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3bd6-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e3bd6-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3bd6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3bd6-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3bd6-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3bd6-131">IDL</span><span class="sxs-lookup"><span data-stu-id="e3bd6-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3bd6-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3bd6-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e3bd6-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3bd6-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3bd6-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e3bd6-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e3bd6-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e3bd6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3bd6-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3bd6-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3bd6-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3bd6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3bd6-138">**Enumerador**</span><span class="sxs-lookup"><span data-stu-id="e3bd6-138">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="e3bd6-139">Enumerar o enumerar todas las instancias de un recurso</span><span class="sxs-lookup"><span data-stu-id="e3bd6-139">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





