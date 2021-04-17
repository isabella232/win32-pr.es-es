---
description: El \_ método get participante obtiene un puntero a una matriz de interfaces ITParticipant que representan los participantes implicados en el evento.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'Método ITParticipantEvent:: get_Participant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680402"
---
# <a name="itparticipanteventget_participant-method"></a><span data-ttu-id="3d27b-103">ITParticipantEvent:: get ( \_ método de participante)</span><span class="sxs-lookup"><span data-stu-id="3d27b-103">ITParticipantEvent::get\_Participant method</span></span>

<span data-ttu-id="3d27b-104">\[**obtener \_ El participante** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3d27b-104">\[**get\_Participant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3d27b-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="3d27b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3d27b-106">El método **Get \_ participante** obtiene un puntero a una matriz de interfaces [**ITParticipant**](itparticipant.md) que representan los participantes implicados en el evento.</span><span class="sxs-lookup"><span data-stu-id="3d27b-106">The **get\_Participant** method gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d27b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d27b-107">Syntax</span></span>


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="3d27b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d27b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d27b-109">*ppParticipant* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3d27b-109">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d27b-110">Puntero a la matriz de interfaces [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="3d27b-110">Pointer to array of [**ITParticipant**](itparticipant.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d27b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d27b-111">Return value</span></span>

<span data-ttu-id="3d27b-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3d27b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3d27b-113">Value</span><span class="sxs-lookup"><span data-stu-id="3d27b-113">Value</span></span>                                                                                           | <span data-ttu-id="3d27b-114">Significado</span><span class="sxs-lookup"><span data-stu-id="3d27b-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d27b-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3d27b-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="3d27b-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3d27b-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="3d27b-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3d27b-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="3d27b-118">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="3d27b-118">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="3d27b-119"><dt>**\_elementos TAPI E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="3d27b-119"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="3d27b-120">No hay participantes asociados al evento.</span><span class="sxs-lookup"><span data-stu-id="3d27b-120">There are no participants associated with the event.</span></span><br/>  |
| <dl> <span data-ttu-id="3d27b-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3d27b-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="3d27b-122">El parámetro *ppParticipant* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="3d27b-122">The *ppParticipant* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3d27b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d27b-123">Requirements</span></span>



| <span data-ttu-id="3d27b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d27b-124">Requirement</span></span> | <span data-ttu-id="3d27b-125">Value</span><span class="sxs-lookup"><span data-stu-id="3d27b-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d27b-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="3d27b-126">TAPI version</span></span><br/> | <span data-ttu-id="3d27b-127">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3d27b-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3d27b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d27b-128">Header</span></span><br/>       | <dl> <span data-ttu-id="3d27b-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d27b-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="3d27b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d27b-130">Library</span></span><br/>      | <dl> <span data-ttu-id="3d27b-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d27b-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3d27b-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d27b-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="3d27b-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d27b-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3d27b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d27b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d27b-135">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="3d27b-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="3d27b-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="3d27b-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




