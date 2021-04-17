---
description: El método Create crea un nuevo medio con propiedades predeterminadas, lo agrega a la colección en el índice especificado y devuelve un puntero a la interfaz ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'ITMediaCollection:: Create (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690978"
---
# <a name="itmediacollectioncreate-method"></a><span data-ttu-id="8a2e3-103">ITMediaCollection:: Create (método)</span><span class="sxs-lookup"><span data-stu-id="8a2e3-103">ITMediaCollection::Create method</span></span>

<span data-ttu-id="8a2e3-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8a2e3-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8a2e3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8a2e3-106">El método **Create** crea un nuevo medio con propiedades predeterminadas, lo agrega a la colección en el índice especificado y devuelve un puntero a la interfaz [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="8a2e3-106">The **Create** method creates a new media with default properties, adds it to the collection at the specified index, and returns a pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a2e3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a2e3-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a><span data-ttu-id="8a2e3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a2e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a2e3-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8a2e3-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a2e3-110">Índice del nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-110">Index for the new item.</span></span> <span data-ttu-id="8a2e3-111">El valor mínimo para el índice es 1 y el valor máximo para el índice es el número actual de elementos + 1.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-111">The minimum value for the index is 1, and the maximum value for the index is the current number of items + 1.</span></span>

</dd> <dt>

<span data-ttu-id="8a2e3-112">*ppMedia* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8a2e3-112">*ppMedia* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a2e3-113">Puntero a la interfaz [**ITMedia**](itmedia.md) creada.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-113">Pointer to [**ITMedia**](itmedia.md) interface created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a2e3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a2e3-114">Return value</span></span>

<span data-ttu-id="8a2e3-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-115">This method can return one of these values.</span></span>



| <span data-ttu-id="8a2e3-116">Value</span><span class="sxs-lookup"><span data-stu-id="8a2e3-116">Value</span></span>                                                                                         | <span data-ttu-id="8a2e3-117">Significado</span><span class="sxs-lookup"><span data-stu-id="8a2e3-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8a2e3-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e3-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8a2e3-119">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8a2e3-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e3-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8a2e3-121">El parámetro *ppMedia* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-121">The *ppMedia* parameter is not a valid pointer.</span></span><br/>      |
| <dl> <span data-ttu-id="8a2e3-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e3-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8a2e3-123">El parámetro de *Índice* no es válido.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="8a2e3-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e3-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8a2e3-125">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8a2e3-126"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e3-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8a2e3-127">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8a2e3-128"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e3-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8a2e3-129">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="8a2e3-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a2e3-130">Remarks</span></span>

<span data-ttu-id="8a2e3-131">La mayoría de las listas de C y C++ están basadas en 0, pero este índice está basado en 1 para la compatibilidad de Visual Basic, lo que significa que el primer elemento tiene un número de índice de 1.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-131">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

<span data-ttu-id="8a2e3-132">TAPI llama al método **AddRef** en la interfaz [**ITMedia**](itmedia.md) devuelta por **ITMediaCollection:: Create**.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-132">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **ITMediaCollection::Create**.</span></span> <span data-ttu-id="8a2e3-133">La aplicación debe llamar a **Release** en la interfaz [**ITMedia**](itmedia.md) para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="8a2e3-133">The application must call **Release** on the [**ITMedia**](itmedia.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a2e3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a2e3-134">Requirements</span></span>



| <span data-ttu-id="8a2e3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a2e3-135">Requirement</span></span> | <span data-ttu-id="8a2e3-136">Value</span><span class="sxs-lookup"><span data-stu-id="8a2e3-136">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2e3-137">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8a2e3-137">TAPI version</span></span><br/> | <span data-ttu-id="8a2e3-138">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8a2e3-138">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8a2e3-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a2e3-139">Header</span></span><br/>       | <dl> <span data-ttu-id="8a2e3-140"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e3-140"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a2e3-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a2e3-141">Library</span></span><br/>      | <dl> <span data-ttu-id="8a2e3-142"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e3-142"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8a2e3-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a2e3-143">DLL</span></span><br/>          | <dl> <span data-ttu-id="8a2e3-144"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a2e3-144"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a2e3-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a2e3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a2e3-146">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="8a2e3-146">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="8a2e3-147">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="8a2e3-147">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




