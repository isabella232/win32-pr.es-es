---
description: El método Delete elimina un componente ITTime.
ms.assetid: 0445d659-7b83-4462-b199-511fd8270f32
title: ITTimeCollection::D método iminar (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9aad562660a2d563193e5074b52f4d1a513bb39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690238"
---
# <a name="ittimecollectiondelete-method"></a><span data-ttu-id="67363-103">ITTimeCollection::D iminar (método)</span><span class="sxs-lookup"><span data-stu-id="67363-103">ITTimeCollection::Delete method</span></span>

<span data-ttu-id="67363-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="67363-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="67363-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="67363-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="67363-106">El método **Delete** elimina un componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="67363-106">The **Delete** method deletes an [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="67363-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67363-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="67363-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67363-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67363-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="67363-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67363-110">Índice del componente [**ITTime**](ittime.md) que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="67363-110">Index of the [**ITTime**](ittime.md) component to be deleted.</span></span> <span data-ttu-id="67363-111">(La matriz de índice está basada en uno).</span><span class="sxs-lookup"><span data-stu-id="67363-111">(The index array is one-based.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67363-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67363-112">Return value</span></span>

<span data-ttu-id="67363-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="67363-113">This method can return one of these values.</span></span>



| <span data-ttu-id="67363-114">Value</span><span class="sxs-lookup"><span data-stu-id="67363-114">Value</span></span>                                                                                         | <span data-ttu-id="67363-115">Significado</span><span class="sxs-lookup"><span data-stu-id="67363-115">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="67363-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="67363-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="67363-117">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="67363-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="67363-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="67363-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="67363-119">El parámetro de *Índice* no es válido.</span><span class="sxs-lookup"><span data-stu-id="67363-119">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="67363-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="67363-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="67363-121">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="67363-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="67363-122"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="67363-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="67363-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="67363-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="67363-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="67363-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="67363-125">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="67363-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="67363-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67363-126">Requirements</span></span>



| <span data-ttu-id="67363-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="67363-127">Requirement</span></span> | <span data-ttu-id="67363-128">Value</span><span class="sxs-lookup"><span data-stu-id="67363-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67363-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="67363-129">TAPI version</span></span><br/> | <span data-ttu-id="67363-130">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="67363-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="67363-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67363-131">Header</span></span><br/>       | <dl> <span data-ttu-id="67363-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="67363-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="67363-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67363-133">Library</span></span><br/>      | <dl> <span data-ttu-id="67363-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67363-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="67363-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67363-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="67363-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67363-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67363-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="67363-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67363-138">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="67363-138">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="67363-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="67363-139">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




