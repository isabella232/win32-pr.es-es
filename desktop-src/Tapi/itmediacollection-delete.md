---
description: El método Delete elimina el medio correspondiente al índice especificado.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: ITMediaCollection::D método iminar (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680506"
---
# <a name="itmediacollectiondelete-method"></a><span data-ttu-id="ad9c7-103">ITMediaCollection::D iminar (método)</span><span class="sxs-lookup"><span data-stu-id="ad9c7-103">ITMediaCollection::Delete method</span></span>

<span data-ttu-id="ad9c7-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ad9c7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ad9c7-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="ad9c7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ad9c7-106">El método **Delete** elimina el medio correspondiente al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="ad9c7-106">The **Delete** method deletes the media corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9c7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad9c7-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="ad9c7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad9c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad9c7-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ad9c7-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9c7-110">Índice de los medios que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="ad9c7-110">Index of media to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad9c7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad9c7-111">Return value</span></span>

<span data-ttu-id="ad9c7-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ad9c7-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ad9c7-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ad9c7-113">Return code</span></span>                                                                                                                              | <span data-ttu-id="ad9c7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad9c7-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad9c7-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c7-115"><dt>**S\_OK**</dt></span></span> </dl>                                                     | <span data-ttu-id="ad9c7-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad9c7-116">Method succeeded.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="ad9c7-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c7-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                             | <span data-ttu-id="ad9c7-118">El parámetro de *Índice* tiene un valor menor que 1 o mayor que el número actual de elementos.</span><span class="sxs-lookup"><span data-stu-id="ad9c7-118">The *Index* parameter has a value less than 1 or greater than the current number of elements.</span></span><br/> |
| <dl> <span data-ttu-id="ad9c7-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c7-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                            | <span data-ttu-id="ad9c7-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="ad9c7-120">Insufficient memory exists to perform the operation.</span></span><br/>                                          |
| <dl> <span data-ttu-id="ad9c7-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c7-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                                   | <span data-ttu-id="ad9c7-122">Error interno (solo se debe producir si una llamada anterior ha devuelto un error).</span><span class="sxs-lookup"><span data-stu-id="ad9c7-122">Internal error (should only occur if a previous call returned an error).</span></span><br/>                      |
| <dl> <span data-ttu-id="ad9c7-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c7-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                                | <span data-ttu-id="ad9c7-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="ad9c7-124">This method is not yet implemented.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ad9c7-125"><dt>**HRESULT \_ del \_ código de error \_ (SDPBLB \_ conf \_ BLOB \_ destruido)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c7-125"><dt>**HRESULT\_FROM\_ERROR\_CODE(SDPBLB\_CONF\_BLOB\_DESTROYED)**</dt></span></span> </dl> | <span data-ttu-id="ad9c7-126">El BLOB SDP no existe.</span><span class="sxs-lookup"><span data-stu-id="ad9c7-126">The SDP blob doesn't exist.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="ad9c7-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad9c7-127">Remarks</span></span>

<span data-ttu-id="ad9c7-128">La mayoría de las listas de C y C++ están basadas en 0, pero este índice está basado en 1 para la compatibilidad de Visual Basic, lo que significa que el primer elemento tiene un número de índice de 1.</span><span class="sxs-lookup"><span data-stu-id="ad9c7-128">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad9c7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad9c7-129">Requirements</span></span>



| <span data-ttu-id="ad9c7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad9c7-130">Requirement</span></span> | <span data-ttu-id="ad9c7-131">Value</span><span class="sxs-lookup"><span data-stu-id="ad9c7-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9c7-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ad9c7-132">TAPI version</span></span><br/> | <span data-ttu-id="ad9c7-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ad9c7-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ad9c7-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad9c7-134">Header</span></span><br/>       | <dl> <span data-ttu-id="ad9c7-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c7-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad9c7-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad9c7-136">Library</span></span><br/>      | <dl> <span data-ttu-id="ad9c7-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c7-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ad9c7-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ad9c7-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="ad9c7-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad9c7-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad9c7-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad9c7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9c7-141">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="ad9c7-141">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




