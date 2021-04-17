---
description: El \_ método get Item obtiene un puntero ITMedia que corresponde al índice especificado.
ms.assetid: ad218357-82c8-4fcb-b71b-ba17564a5ca5
title: 'Método ITMediaCollection:: get_Item (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c68f3571dbd1f66e325dd7fa1bb30dfe6d6bc35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690623"
---
# <a name="itmediacollectionget_item-method"></a><span data-ttu-id="05ba6-103">ITMediaCollection:: get \_ Item (método)</span><span class="sxs-lookup"><span data-stu-id="05ba6-103">ITMediaCollection::get\_Item method</span></span>

<span data-ttu-id="05ba6-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="05ba6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="05ba6-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="05ba6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="05ba6-106">El método **Get \_ Item** obtiene un puntero [**ITMedia**](itmedia.md) que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="05ba6-106">The **get\_Item** method gets an [**ITMedia**](itmedia.md) pointer corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="05ba6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05ba6-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG    Index,
  [out] ITMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="05ba6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05ba6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05ba6-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="05ba6-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05ba6-110">Índice del elemento multimedia que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="05ba6-110">Index of media item to get.</span></span>

</dd> <dt>

<span data-ttu-id="05ba6-111">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="05ba6-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05ba6-112">Puntero a la interfaz [**ITMedia**](itmedia.md) para el elemento deseado.</span><span class="sxs-lookup"><span data-stu-id="05ba6-112">Pointer to the [**ITMedia**](itmedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05ba6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05ba6-113">Return value</span></span>

<span data-ttu-id="05ba6-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="05ba6-114">This method can return one of these values.</span></span>



| <span data-ttu-id="05ba6-115">Value</span><span class="sxs-lookup"><span data-stu-id="05ba6-115">Value</span></span>                                                                                         | <span data-ttu-id="05ba6-116">Significado</span><span class="sxs-lookup"><span data-stu-id="05ba6-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="05ba6-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="05ba6-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="05ba6-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="05ba6-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="05ba6-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="05ba6-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="05ba6-120">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="05ba6-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="05ba6-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="05ba6-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="05ba6-122">El parámetro de *Índice* no es válido.</span><span class="sxs-lookup"><span data-stu-id="05ba6-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="05ba6-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="05ba6-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="05ba6-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="05ba6-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="05ba6-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="05ba6-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="05ba6-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="05ba6-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="05ba6-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="05ba6-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="05ba6-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="05ba6-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="05ba6-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05ba6-129">Remarks</span></span>

<span data-ttu-id="05ba6-130">La mayoría de las listas de C y C++ están basadas en 0, pero este índice está basado en 1 para la compatibilidad de Visual Basic, lo que significa que el primer elemento tiene un número de índice de 1.</span><span class="sxs-lookup"><span data-stu-id="05ba6-130">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="05ba6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05ba6-131">Requirements</span></span>



| <span data-ttu-id="05ba6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="05ba6-132">Requirement</span></span> | <span data-ttu-id="05ba6-133">Value</span><span class="sxs-lookup"><span data-stu-id="05ba6-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05ba6-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="05ba6-134">TAPI version</span></span><br/> | <span data-ttu-id="05ba6-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="05ba6-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="05ba6-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05ba6-136">Header</span></span><br/>       | <dl> <span data-ttu-id="05ba6-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="05ba6-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="05ba6-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05ba6-138">Library</span></span><br/>      | <dl> <span data-ttu-id="05ba6-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05ba6-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="05ba6-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05ba6-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="05ba6-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05ba6-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05ba6-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="05ba6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ba6-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="05ba6-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="05ba6-144">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="05ba6-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




