---
description: La plantilla de clase IMediaObjectImpl proporciona una implementación base para la interfaz IMediaObject. Para obtener más información sobre el uso de esta plantilla, vea uso de la plantilla de clase DMO.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Plantilla de clase IMediaObjectImpl (Dmoimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680617"
---
# <a name="imediaobjectimpl-class-template"></a><span data-ttu-id="73dc5-104">Plantilla de clase IMediaObjectImpl</span><span class="sxs-lookup"><span data-stu-id="73dc5-104">IMediaObjectImpl Class Template</span></span>

<span data-ttu-id="73dc5-105">La `IMediaObjectImpl` plantilla de clase proporciona una implementación base para la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="73dc5-105">The `IMediaObjectImpl` class template provides a base implementation for the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="73dc5-106">Para obtener más información sobre el uso de esta plantilla, vea [uso de la plantilla de clase DMO](using-the-dmo-class-template.md).</span><span class="sxs-lookup"><span data-stu-id="73dc5-106">For more information on using this template, see [Using the DMO Class Template](using-the-dmo-class-template.md).</span></span>

<span data-ttu-id="73dc5-107">Esta `IMediaObjectImpl` plantilla expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="73dc5-107">This `IMediaObjectImpl` template exposes the following members.</span></span>



| <span data-ttu-id="73dc5-108">Clase anidada</span><span class="sxs-lookup"><span data-stu-id="73dc5-108">Nested Class</span></span>                              | <span data-ttu-id="73dc5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="73dc5-109">Description</span></span>                                  |
|-------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="73dc5-110">**LockIt**</span><span class="sxs-lookup"><span data-stu-id="73dc5-110">**LockIt**</span></span>](imediaobjectimpl-lockit.md) | <span data-ttu-id="73dc5-111">Clase auxiliar que bloquea y desbloquea DMO.</span><span class="sxs-lookup"><span data-stu-id="73dc5-111">Helper class that locks and unlocks the DMO.</span></span> |



 



| <span data-ttu-id="73dc5-112">Método</span><span class="sxs-lookup"><span data-stu-id="73dc5-112">Method</span></span>                                                                      | <span data-ttu-id="73dc5-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="73dc5-113">Description</span></span>                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="73dc5-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73dc5-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span></span>                     | <span data-ttu-id="73dc5-115">Determina si todas las secuencias no opcionales tienen tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="73dc5-115">Determines whether all of the non-optional streams have media types.</span></span> |
| <span data-ttu-id="73dc5-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73dc5-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span></span>                             | <span data-ttu-id="73dc5-117">Recupera el tipo de medio actual para un flujo de entrada especificado.</span><span class="sxs-lookup"><span data-stu-id="73dc5-117">Retrieves the current media type for a specified input stream.</span></span>       |
| <span data-ttu-id="73dc5-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73dc5-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span></span>                       | <span data-ttu-id="73dc5-119">Consulta si el tipo de medio se estableció en un flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="73dc5-119">Queries whether the media type was set on an input stream.</span></span>           |
| <span data-ttu-id="73dc5-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73dc5-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span></span>   | <span data-ttu-id="73dc5-121">Consulta si un flujo de entrada puede aceptar más entradas.</span><span class="sxs-lookup"><span data-stu-id="73dc5-121">Queries whether an input stream can accept more input.</span></span>               |
| <span data-ttu-id="73dc5-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73dc5-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span></span>   | <span data-ttu-id="73dc5-123">Consulta si un flujo de entrada puede aceptar un tipo de medio determinado.</span><span class="sxs-lookup"><span data-stu-id="73dc5-123">Queries whether an input stream can accept a given media type.</span></span>       |
| <span data-ttu-id="73dc5-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73dc5-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span></span> | <span data-ttu-id="73dc5-125">Consulta si un flujo de salida puede aceptar un tipo de medio determinado.</span><span class="sxs-lookup"><span data-stu-id="73dc5-125">Queries whether an output stream can accept a given media type.</span></span>      |
| <span data-ttu-id="73dc5-126">[**Lock**](/previous-versions/ms809100(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73dc5-126">[**Lock**](/previous-versions/ms809100(v=msdn.10))</span></span>                                       | <span data-ttu-id="73dc5-127">Bloquea DMO</span><span class="sxs-lookup"><span data-stu-id="73dc5-127">Locks the DMO</span></span>                                                        |
| <span data-ttu-id="73dc5-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73dc5-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span></span>                           | <span data-ttu-id="73dc5-129">Recupera el tipo de medio actual para un flujo de salida especificado.</span><span class="sxs-lookup"><span data-stu-id="73dc5-129">Retrieves the current media type for a specified output stream.</span></span>      |
| <span data-ttu-id="73dc5-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73dc5-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span></span>                     | <span data-ttu-id="73dc5-131">Consulta si el tipo de medio se estableció en un flujo de salida.</span><span class="sxs-lookup"><span data-stu-id="73dc5-131">Queries whether the media type was set on an output stream.</span></span>          |
| <span data-ttu-id="73dc5-132">[**Pulsa**](/previous-versions/ms809101(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73dc5-132">[**Unlock**](/previous-versions/ms809101(v=msdn.10))</span></span>                                   | <span data-ttu-id="73dc5-133">Desbloquea DMO</span><span class="sxs-lookup"><span data-stu-id="73dc5-133">Unlocks the DMO</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="73dc5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73dc5-134">Requirements</span></span>



| <span data-ttu-id="73dc5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="73dc5-135">Requirement</span></span> | <span data-ttu-id="73dc5-136">Value</span><span class="sxs-lookup"><span data-stu-id="73dc5-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73dc5-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73dc5-137">Header</span></span><br/>  | <dl> <span data-ttu-id="73dc5-138"><dt>Dmoimpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73dc5-138"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="73dc5-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73dc5-139">Library</span></span><br/> | <dl> <span data-ttu-id="73dc5-140"><dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73dc5-140"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73dc5-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="73dc5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73dc5-142">Referencia de DMO</span><span class="sxs-lookup"><span data-stu-id="73dc5-142">DMO Reference</span></span>](dmo-reference.md)
</dt> <dt>

[<span data-ttu-id="73dc5-143">Uso de la plantilla de clase DMO</span><span class="sxs-lookup"><span data-stu-id="73dc5-143">Using the DMO Class Template</span></span>](using-the-dmo-class-template.md)
</dt> </dl>

 

 
