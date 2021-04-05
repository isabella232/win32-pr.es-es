---
title: Propiedad TargetName de ITsSbTarget
description: Especifica o recupera el nombre del destino.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Propiedad TargetName Servicios de Escritorio remoto
- Propiedad TargetName Servicios de Escritorio remoto, interfaz ITsSbTarget
- Servicios de Escritorio remoto de la interfaz ITsSbTarget, propiedad TargetName
- Propiedad TargetName Servicios de Escritorio remoto, interfaz ITsSbTargetEx
- Servicios de Escritorio remoto de la interfaz ITsSbTargetEx, propiedad TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dce949abee4ca00184a2b784ab154dbd75b9de6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076927"
---
# <a name="itssbtargettargetname-property"></a><span data-ttu-id="248e5-108">ITsSbTarget:: TargetName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="248e5-108">ITsSbTarget::TargetName property</span></span>

<span data-ttu-id="248e5-109">Especifica o recupera el nombre del destino.</span><span class="sxs-lookup"><span data-stu-id="248e5-109">Specifies or retrieves the name of the target.</span></span>

<span data-ttu-id="248e5-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="248e5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="248e5-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="248e5-111">Syntax</span></span>


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="248e5-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="248e5-112">Property value</span></span>

<span data-ttu-id="248e5-113">Variable **BSTR** que especifica el nombre de destino.</span><span class="sxs-lookup"><span data-stu-id="248e5-113">A **BSTR** variable that specifies the target name.</span></span>

## <a name="remarks"></a><span data-ttu-id="248e5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="248e5-114">Remarks</span></span>

<span data-ttu-id="248e5-115">Esta propiedad era de solo lectura antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="248e5-115">This property was read-only prior to Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="248e5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="248e5-116">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="248e5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="248e5-117">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="248e5-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="248e5-118">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="248e5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="248e5-119">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="248e5-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="248e5-120">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="248e5-121">IDL</span><span class="sxs-lookup"><span data-stu-id="248e5-121">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="248e5-122"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="248e5-122"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="248e5-123">IID</span><span class="sxs-lookup"><span data-stu-id="248e5-123">IID</span></span><br/></td>
<td><span data-ttu-id="248e5-124">IID_ITsSbTarget se define como:</span><span class="sxs-lookup"><span data-stu-id="248e5-124">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="248e5-125">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="248e5-125">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="248e5-126">e85e10ea-db0b-4752-B456-5fd5840901c0 en Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="248e5-126">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="248e5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="248e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="248e5-128">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="248e5-128">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="248e5-129">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="248e5-129">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





