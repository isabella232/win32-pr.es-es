---
title: Constantes del recopilador de eventos de Windows (Evcoll. h)
description: El SDK del recopilador de eventos de Windows contiene las siguientes constantes.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800956"
---
# <a name="windows-event-collector-constants"></a><span data-ttu-id="31466-103">Constantes del recopilador de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="31466-103">Windows Event Collector Constants</span></span>

<span data-ttu-id="31466-104">El SDK del recopilador de eventos de Windows contiene las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="31466-104">The Windows Event Collector SDK contains the following constants.</span></span>

<dl> <dt>

<span data-ttu-id="31466-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**\_máscara de \_ tipo \_ variante de EC**</span><span class="sxs-lookup"><span data-stu-id="31466-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31466-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="31466-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="31466-107">Se usa para enmascarar el bit de la matriz desde la propiedad **Type** de una [**\_ variante EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) para extraer el tipo del valor Variant.</span><span class="sxs-lookup"><span data-stu-id="31466-107">Used to mask out the array bit from the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) to extract the type of the variant value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31466-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**\_matriz de \_ tipo \_ Variant de EC**</span><span class="sxs-lookup"><span data-stu-id="31466-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31466-109">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="31466-109">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="31466-110">Cuando este bit se establece en la propiedad **Type** de una [**\_ variante EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), la variante contiene un puntero a una matriz de valores, en lugar del propio valor.</span><span class="sxs-lookup"><span data-stu-id="31466-110">When this bit is set in the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31466-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**\_acceso de lectura de EC \_**</span><span class="sxs-lookup"><span data-stu-id="31466-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31466-112">1</span><span class="sxs-lookup"><span data-stu-id="31466-112">1</span></span>
</dt> <dt>



<span data-ttu-id="31466-113">Permiso de control de acceso de lectura que permite leer información del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="31466-113">Read access control permission that allows information to be read from the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31466-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_acceso de escritura de EC \_**</span><span class="sxs-lookup"><span data-stu-id="31466-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31466-115">2</span><span class="sxs-lookup"><span data-stu-id="31466-115">2</span></span>
</dt> <dt>



<span data-ttu-id="31466-116">Permiso de control de acceso de escritura que permite escribir información en el recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="31466-116">Write access control permission that allows information to be written to the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31466-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ abrir \_ siempre**</span><span class="sxs-lookup"><span data-stu-id="31466-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC\_OPEN\_ALWAYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31466-118">0</span><span class="sxs-lookup"><span data-stu-id="31466-118">0</span></span>
</dt> <dt>



<span data-ttu-id="31466-119">Abre una suscripción existente o crea la suscripción si no existe.</span><span class="sxs-lookup"><span data-stu-id="31466-119">Opens an existing subscription or creates the subscription if it does not exist.</span></span> <span data-ttu-id="31466-120">Lo usa el método [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="31466-120">Used by the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31466-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**\_crear \_ nuevo**</span><span class="sxs-lookup"><span data-stu-id="31466-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC\_CREATE\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31466-122">1</span><span class="sxs-lookup"><span data-stu-id="31466-122">1</span></span>
</dt> <dt>



<span data-ttu-id="31466-123">Una marca pasada a la función [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) que especifica que se debe crear una nueva suscripción.</span><span class="sxs-lookup"><span data-stu-id="31466-123">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that a new subscription should be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31466-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ abierto \_ existente**</span><span class="sxs-lookup"><span data-stu-id="31466-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC\_OPEN\_EXISTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31466-125">2</span><span class="sxs-lookup"><span data-stu-id="31466-125">2</span></span>
</dt> <dt>



<span data-ttu-id="31466-126">Una marca pasada a la función [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) que especifica que se debe abrir una suscripción existente.</span><span class="sxs-lookup"><span data-stu-id="31466-126">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that an existing subscription should be opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31466-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31466-127">Requirements</span></span>



| <span data-ttu-id="31466-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="31466-128">Requirement</span></span> | <span data-ttu-id="31466-129">Value</span><span class="sxs-lookup"><span data-stu-id="31466-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31466-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31466-130">Minimum supported client</span></span><br/> | <span data-ttu-id="31466-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31466-131">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="31466-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31466-132">Minimum supported server</span></span><br/> | <span data-ttu-id="31466-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31466-133">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="31466-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31466-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="31466-135"><dt>Evcoll. h</dt></span><span class="sxs-lookup"><span data-stu-id="31466-135"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





