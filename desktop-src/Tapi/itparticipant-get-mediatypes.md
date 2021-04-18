---
description: El \_ método get MediaTypes obtiene los tipos de medios asociados a un participante.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'Método ITParticipant:: get_MediaTypes (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678935"
---
# <a name="itparticipantget_mediatypes-method"></a><span data-ttu-id="e0f08-103">ITParticipant:: get \_ MediaTypes (método)</span><span class="sxs-lookup"><span data-stu-id="e0f08-103">ITParticipant::get\_MediaTypes method</span></span>

<span data-ttu-id="e0f08-104">\[**obtener \_ MediaTypes** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e0f08-104">\[**get\_MediaTypes** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e0f08-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e0f08-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e0f08-106">El método **Get \_ MediaTypes** obtiene los [**tipos de medios**](tapimediatype--constants.md) asociados a un participante.</span><span class="sxs-lookup"><span data-stu-id="e0f08-106">The **get\_MediaTypes** method gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f08-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0f08-107">Syntax</span></span>


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="e0f08-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0f08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0f08-109">*plMediaType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e0f08-109">*plMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0f08-110">Puntero a marcas de tipo de medio, como TAPIMEDIATYPE \_ video.</span><span class="sxs-lookup"><span data-stu-id="e0f08-110">Pointer to media type flags, such as TAPIMEDIATYPE\_VIDEO.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0f08-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0f08-111">Return value</span></span>

<span data-ttu-id="e0f08-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e0f08-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e0f08-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e0f08-113">Return code</span></span>                                                                                   | <span data-ttu-id="e0f08-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0f08-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e0f08-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e0f08-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e0f08-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0f08-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e0f08-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e0f08-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e0f08-118">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="e0f08-118">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e0f08-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e0f08-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e0f08-120">El parámetro *plMediaType* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="e0f08-120">The *plMediaType* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="e0f08-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0f08-121">Requirements</span></span>



| <span data-ttu-id="e0f08-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0f08-122">Requirement</span></span> | <span data-ttu-id="e0f08-123">Value</span><span class="sxs-lookup"><span data-stu-id="e0f08-123">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f08-124">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="e0f08-124">TAPI version</span></span><br/> | <span data-ttu-id="e0f08-125">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e0f08-125">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="e0f08-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0f08-126">Header</span></span><br/>       | <dl> <span data-ttu-id="e0f08-127"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0f08-127"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0f08-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0f08-128">Library</span></span><br/>      | <dl> <span data-ttu-id="e0f08-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0f08-129"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e0f08-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0f08-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="e0f08-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0f08-131"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f08-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0f08-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f08-133">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="e0f08-133">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="e0f08-134">**tipos de medios**</span><span class="sxs-lookup"><span data-stu-id="e0f08-134">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

 




