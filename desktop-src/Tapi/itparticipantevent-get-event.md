---
description: El \_ método get Event obtiene un \_ descriptor de eventos de participante del tipo de evento que se ha producido.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'Método ITParticipantEvent:: get_Event (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690830"
---
# <a name="itparticipanteventget_event-method"></a><span data-ttu-id="2e2ff-103">ITParticipantEvent:: get ( \_ método de eventos)</span><span class="sxs-lookup"><span data-stu-id="2e2ff-103">ITParticipantEvent::get\_Event method</span></span>

<span data-ttu-id="2e2ff-104">\[**obtener \_ El evento** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-104">\[**get\_Event** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2e2ff-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2e2ff-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2e2ff-106">El método **Get \_ Event** obtiene un descriptor de [**\_ eventos de participante**](participant-event.md) del tipo de evento que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-106">The **get\_Event** method gets a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the type of event that has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2ff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e2ff-107">Syntax</span></span>


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a><span data-ttu-id="2e2ff-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e2ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e2ff-109">*pParticipantEvent* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e2ff-109">*pParticipantEvent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e2ff-110">Puntero a un descriptor de [**\_ eventos de participante**](participant-event.md) del evento.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-110">Pointer to a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e2ff-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e2ff-111">Return value</span></span>

<span data-ttu-id="2e2ff-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2e2ff-113">Value</span><span class="sxs-lookup"><span data-stu-id="2e2ff-113">Value</span></span>                                                                                         | <span data-ttu-id="2e2ff-114">Significado</span><span class="sxs-lookup"><span data-stu-id="2e2ff-114">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="2e2ff-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2ff-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2e2ff-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-116">Method succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="2e2ff-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2ff-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2e2ff-118">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-118">Insufficient memory exists to perform the operation.</span></span><br/>      |
| <dl> <span data-ttu-id="2e2ff-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2ff-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2e2ff-120">El parámetro *pParticipantEvent* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-120">The *pParticipantEvent* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2e2ff-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e2ff-121">Requirements</span></span>



| <span data-ttu-id="2e2ff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e2ff-122">Requirement</span></span> | <span data-ttu-id="2e2ff-123">Value</span><span class="sxs-lookup"><span data-stu-id="2e2ff-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2ff-124">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="2e2ff-124">TAPI version</span></span><br/> | <span data-ttu-id="2e2ff-125">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="2e2ff-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2e2ff-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e2ff-126">Header</span></span><br/>       | <dl> <span data-ttu-id="2e2ff-127"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2ff-127"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="2e2ff-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e2ff-128">Library</span></span><br/>      | <dl> <span data-ttu-id="2e2ff-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e2ff-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2e2ff-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e2ff-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="2e2ff-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e2ff-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2e2ff-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e2ff-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2ff-133">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="2e2ff-133">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="2e2ff-134">**evento de participante \_**</span><span class="sxs-lookup"><span data-stu-id="2e2ff-134">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> </dl>

 

 




