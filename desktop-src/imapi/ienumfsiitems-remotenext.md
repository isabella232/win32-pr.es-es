---
title: IEnumFsiItems RemoteNext, método
description: Admite un cliente remoto que desea recuperar un número especificado de elementos en la secuencia de enumeración. | IEnumFsiItems RemoteNext, método
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- Método RemoteNext IMAPi
- Método RemoteNext IMAPi, interfaz IEnumFsiItems
- Interfaz IEnumFsiItems IMAPi, método RemoteNext
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e29d3f75cd8e2f83fcd21236661d0d1fa0dabef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547643"
---
# <a name="ienumfsiitemsremotenext-method"></a><span data-ttu-id="45cfd-107">IEnumFsiItems:: RemoteNext (método)</span><span class="sxs-lookup"><span data-stu-id="45cfd-107">IEnumFsiItems::RemoteNext method</span></span>

<span data-ttu-id="45cfd-108">Admite un cliente remoto que desea recuperar un número especificado de elementos en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="45cfd-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cfd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45cfd-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="45cfd-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45cfd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45cfd-111">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45cfd-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45cfd-112">Número de elementos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="45cfd-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="45cfd-113">*rgelt* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="45cfd-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45cfd-114">Matriz de interfaces [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) .</span><span class="sxs-lookup"><span data-stu-id="45cfd-114">Array of [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) interfaces.</span></span> <span data-ttu-id="45cfd-115">Debe liberar cada interfaz en rgelt cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="45cfd-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="45cfd-116">*pceltFetched* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="45cfd-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45cfd-117">Número de elementos devueltos en rgelt.</span><span class="sxs-lookup"><span data-stu-id="45cfd-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="45cfd-118">Puede establecer *pceltFetched* en **null** si *Celt* es uno.</span><span class="sxs-lookup"><span data-stu-id="45cfd-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="45cfd-119">De lo contrario, inicialice el valor de *pceltFetched* en 0 antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="45cfd-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45cfd-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45cfd-120">Return value</span></span>

<span data-ttu-id="45cfd-121">\_Se devuelve S OK cuando el número de elementos solicitados (*Celt*) se devuelve correctamente o el número de elementos devueltos (*pceltFetched*) es menor que el número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="45cfd-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="45cfd-122">Se pueden devolver otros códigos de éxito como resultado de la implementación de.</span><span class="sxs-lookup"><span data-stu-id="45cfd-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="45cfd-123">Los códigos de error siguientes se suelen devolver en caso de error en la operación, pero no representan los únicos valores de error posibles:</span><span class="sxs-lookup"><span data-stu-id="45cfd-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="45cfd-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="45cfd-124">Return code</span></span>                                                                                   | <span data-ttu-id="45cfd-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="45cfd-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45cfd-126"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="45cfd-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="45cfd-127">El puntero no es válido.</span><span class="sxs-lookup"><span data-stu-id="45cfd-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="45cfd-128">Valor: 0x80004003</span><span class="sxs-lookup"><span data-stu-id="45cfd-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="45cfd-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="45cfd-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="45cfd-130">No se pudo asignar la memoria necesaria.</span><span class="sxs-lookup"><span data-stu-id="45cfd-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="45cfd-131">Valor: 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="45cfd-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="45cfd-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="45cfd-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="45cfd-133">Uno o varios argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="45cfd-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="45cfd-134">Valor: 0x80070057</span><span class="sxs-lookup"><span data-stu-id="45cfd-134">Value: 0x80070057</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="45cfd-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45cfd-135">Requirements</span></span>



| <span data-ttu-id="45cfd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="45cfd-136">Requirement</span></span> | <span data-ttu-id="45cfd-137">Value</span><span class="sxs-lookup"><span data-stu-id="45cfd-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45cfd-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45cfd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="45cfd-139">Windows Vista, Windows XP con \[ solo aplicaciones de escritorio de SP2\]</span><span class="sxs-lookup"><span data-stu-id="45cfd-139">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="45cfd-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45cfd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="45cfd-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="45cfd-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="45cfd-142">IDL</span><span class="sxs-lookup"><span data-stu-id="45cfd-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45cfd-143"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45cfd-143"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45cfd-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="45cfd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45cfd-145">**IEnumFsiItems**</span><span class="sxs-lookup"><span data-stu-id="45cfd-145">**IEnumFsiItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[<span data-ttu-id="45cfd-146">IEnumFsiItems:: Next</span><span class="sxs-lookup"><span data-stu-id="45cfd-146">IEnumFsiItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





