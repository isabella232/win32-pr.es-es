---
description: El \_ método get participantes crea una colección de participantes asociados a la Conferencia actual.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'Método ITParticipantControl:: get_Participants (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690307"
---
# <a name="itparticipantcontrolget_participants-method"></a><span data-ttu-id="2319d-103">ITParticipantControl:: get ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="2319d-103">ITParticipantControl::get\_Participants method</span></span>

<span data-ttu-id="2319d-104">\[**obtener \_ Los participantes** no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2319d-104">\[**get\_Participants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2319d-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2319d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2319d-106">El método **Get \_ participantes** crea una colección de participantes asociados a la Conferencia actual.</span><span class="sxs-lookup"><span data-stu-id="2319d-106">The **get\_Participants** method creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="2319d-107">Este método se proporciona para las aplicaciones cliente de automatización, como las escritas en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2319d-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="2319d-108">Las aplicaciones de C y C++ deben usar el método [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) .</span><span class="sxs-lookup"><span data-stu-id="2319d-108">C and C++ applications must use the [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2319d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2319d-109">Syntax</span></span>


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="2319d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2319d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2319d-111">*pVariant* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2319d-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2319d-112">Puntero a **Variant** que contiene un [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de punteros de la interfaz [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="2319d-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2319d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2319d-113">Return value</span></span>

<span data-ttu-id="2319d-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2319d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2319d-115">Value</span><span class="sxs-lookup"><span data-stu-id="2319d-115">Value</span></span>                                                                                         | <span data-ttu-id="2319d-116">Significado</span><span class="sxs-lookup"><span data-stu-id="2319d-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2319d-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2319d-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2319d-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2319d-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2319d-120">El parámetro *pVariant* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="2319d-120">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |
| <dl> <span data-ttu-id="2319d-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2319d-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="2319d-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2319d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2319d-123">Remarks</span></span>

<span data-ttu-id="2319d-124">TAPI llama al método **AddRef** en la interfaz [**ITParticipant**](itparticipant.md) devuelta por **ITParticipantControl:: get \_ participantes**.</span><span class="sxs-lookup"><span data-stu-id="2319d-124">TAPI calls the **AddRef** method on the [**ITParticipant**](itparticipant.md) interface returned by **ITParticipantControl::get\_Participants**.</span></span> <span data-ttu-id="2319d-125">La aplicación debe llamar a **Release** en la interfaz **ITParticipant** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="2319d-125">The application must call **Release** on the **ITParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2319d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2319d-126">Requirements</span></span>



| <span data-ttu-id="2319d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2319d-127">Requirement</span></span> | <span data-ttu-id="2319d-128">Value</span><span class="sxs-lookup"><span data-stu-id="2319d-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2319d-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="2319d-129">TAPI version</span></span><br/> | <span data-ttu-id="2319d-130">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="2319d-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2319d-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2319d-131">Header</span></span><br/>       | <dl> <span data-ttu-id="2319d-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="2319d-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2319d-133">Library</span></span><br/>      | <dl> <span data-ttu-id="2319d-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2319d-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2319d-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="2319d-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2319d-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2319d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2319d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2319d-138">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="2319d-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="2319d-139">**EnumerateParticipants**</span><span class="sxs-lookup"><span data-stu-id="2319d-139">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[<span data-ttu-id="2319d-140">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="2319d-140">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="2319d-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="2319d-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




