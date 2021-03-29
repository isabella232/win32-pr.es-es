---
description: 'La interfaz IEnumParticipant proporciona métodos de enumeración estándar de COM para la interfaz ITParticipant. El método ITParticipantControl:: EnumerateParticipants devuelve un puntero a IEnumParticipant.'
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Interfaz IEnumParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680700"
---
# <a name="ienumparticipant-interface"></a><span data-ttu-id="f259e-104">Interfaz IEnumParticipant</span><span class="sxs-lookup"><span data-stu-id="f259e-104">IEnumParticipant interface</span></span>

<span data-ttu-id="f259e-105">\[**IEnumParticipant** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f259e-105">\[**IEnumParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f259e-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f259e-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f259e-107">La interfaz **IEnumParticipant** proporciona métodos de enumeración estándar de com para la interfaz [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="f259e-107">The **IEnumParticipant** interface provides COM-standard enumeration methods for the [**ITParticipant**](itparticipant.md) interface.</span></span> <span data-ttu-id="f259e-108">El método [**ITParticipantControl:: EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) devuelve un puntero a **IEnumParticipant**.</span><span class="sxs-lookup"><span data-stu-id="f259e-108">The [**ITParticipantControl::EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method returns a pointer to **IEnumParticipant**.</span></span>

<span data-ttu-id="f259e-109">La interfaz **IEnumParticipant** se oculta en Visual Basic y en los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="f259e-109">The **IEnumParticipant** interface is hidden from Visual Basic and scripting languages.</span></span>

## <a name="members"></a><span data-ttu-id="f259e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f259e-110">Members</span></span>

<span data-ttu-id="f259e-111">La interfaz **IEnumParticipant** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f259e-111">The **IEnumParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f259e-112">**IEnumParticipant** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f259e-112">**IEnumParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="f259e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f259e-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f259e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="f259e-114">Methods</span></span>

<span data-ttu-id="f259e-115">La interfaz **IEnumParticipant** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f259e-115">The **IEnumParticipant** interface has these methods.</span></span>



| <span data-ttu-id="f259e-116">Método</span><span class="sxs-lookup"><span data-stu-id="f259e-116">Method</span></span>                                  | <span data-ttu-id="f259e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f259e-117">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f259e-118">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="f259e-118">**Clone**</span></span>](ienumparticipant-clone.md) | <span data-ttu-id="f259e-119">Crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="f259e-119">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="f259e-120">**Next**</span><span class="sxs-lookup"><span data-stu-id="f259e-120">**Next**</span></span>](ienumparticipant-next.md)   | <span data-ttu-id="f259e-121">Obtiene el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="f259e-121">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="f259e-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="f259e-122">**Reset**</span></span>](ienumparticipant-reset.md) | <span data-ttu-id="f259e-123">Se restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="f259e-123">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="f259e-124">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="f259e-124">**Skip**</span></span>](ienumparticipant-skip.md)   | <span data-ttu-id="f259e-125">Omite el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="f259e-125">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="f259e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f259e-126">Requirements</span></span>



| <span data-ttu-id="f259e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f259e-127">Requirement</span></span> | <span data-ttu-id="f259e-128">Value</span><span class="sxs-lookup"><span data-stu-id="f259e-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f259e-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f259e-129">TAPI version</span></span><br/> | <span data-ttu-id="f259e-130">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f259e-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f259e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f259e-131">Header</span></span><br/>       | <dl> <span data-ttu-id="f259e-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="f259e-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="f259e-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f259e-133">Library</span></span><br/>      | <dl> <span data-ttu-id="f259e-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f259e-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f259e-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f259e-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="f259e-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f259e-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f259e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f259e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f259e-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="f259e-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

