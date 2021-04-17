---
description: El método EnumerateParticipants enumera los participantes asociados a la Conferencia actual.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'ITParticipantControl:: EnumerateParticipants (método) (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689986"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a><span data-ttu-id="9bce5-103">ITParticipantControl:: EnumerateParticipants (método)</span><span class="sxs-lookup"><span data-stu-id="9bce5-103">ITParticipantControl::EnumerateParticipants method</span></span>

<span data-ttu-id="9bce5-104">\[**EnumerateParticipants** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9bce5-104">\[**EnumerateParticipants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9bce5-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="9bce5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9bce5-106">El método **EnumerateParticipants** enumera los participantes asociados a la Conferencia actual.</span><span class="sxs-lookup"><span data-stu-id="9bce5-106">The **EnumerateParticipants** method enumerates participants associated with the current conference.</span></span> <span data-ttu-id="9bce5-107">Este método se proporciona para las aplicaciones de C y C++.</span><span class="sxs-lookup"><span data-stu-id="9bce5-107">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="9bce5-108">Las aplicaciones cliente de automatización, como las escritas en Visual Basic, deben usar el método [**Get \_ participantes**](itparticipantcontrol-get-participants.md) .</span><span class="sxs-lookup"><span data-stu-id="9bce5-108">Automation client applications, such as those written in Visual Basic, must use the [**get\_Participants**](itparticipantcontrol-get-participants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bce5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9bce5-109">Syntax</span></span>


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a><span data-ttu-id="9bce5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9bce5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bce5-111">*ppEnumParticipants* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9bce5-111">*ppEnumParticipants* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bce5-112">Puntero a la interfaz [**IEnumParticipant**](ienumparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="9bce5-112">Pointer to [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bce5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9bce5-113">Return value</span></span>

<span data-ttu-id="9bce5-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="9bce5-114">This method can return one of these values.</span></span>



| <span data-ttu-id="9bce5-115">Value</span><span class="sxs-lookup"><span data-stu-id="9bce5-115">Value</span></span>                                                                                         | <span data-ttu-id="9bce5-116">Significado</span><span class="sxs-lookup"><span data-stu-id="9bce5-116">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="9bce5-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9bce5-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9bce5-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9bce5-118">Method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="9bce5-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="9bce5-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9bce5-120">El parámetro *ppEnumParticipants* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="9bce5-120">The *ppEnumParticipants* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="9bce5-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9bce5-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9bce5-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="9bce5-122">Insufficient memory exists to perform the operation.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="9bce5-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9bce5-123">Remarks</span></span>

<span data-ttu-id="9bce5-124">TAPI llama al método **AddRef** en la interfaz [**IEnumParticipant**](ienumparticipant.md) devuelta por **ITParticipantControl:: EnumerateParticipants**.</span><span class="sxs-lookup"><span data-stu-id="9bce5-124">TAPI calls the **AddRef** method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **ITParticipantControl::EnumerateParticipants**.</span></span> <span data-ttu-id="9bce5-125">La aplicación debe llamar a **Release** en la interfaz **IEnumParticipant** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="9bce5-125">The application must call **Release** on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bce5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bce5-126">Requirements</span></span>



| <span data-ttu-id="9bce5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bce5-127">Requirement</span></span> | <span data-ttu-id="9bce5-128">Value</span><span class="sxs-lookup"><span data-stu-id="9bce5-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bce5-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="9bce5-129">TAPI version</span></span><br/> | <span data-ttu-id="9bce5-130">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="9bce5-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9bce5-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9bce5-131">Header</span></span><br/>       | <dl> <span data-ttu-id="9bce5-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bce5-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="9bce5-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9bce5-133">Library</span></span><br/>      | <dl> <span data-ttu-id="9bce5-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bce5-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9bce5-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9bce5-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="9bce5-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bce5-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9bce5-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bce5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bce5-138">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="9bce5-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="9bce5-139">**obtener \_ participantes**</span><span class="sxs-lookup"><span data-stu-id="9bce5-139">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)
</dt> <dt>

[<span data-ttu-id="9bce5-140">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="9bce5-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="9bce5-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="9bce5-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




