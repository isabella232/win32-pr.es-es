---
description: El \_ método get streams crea una colección de secuencias asociadas al participante actual.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'Método ITParticipant:: get_Streams (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680172"
---
# <a name="itparticipantget_streams-method"></a><span data-ttu-id="59b18-103">ITParticipant:: get \_ streams (método)</span><span class="sxs-lookup"><span data-stu-id="59b18-103">ITParticipant::get\_Streams method</span></span>

<span data-ttu-id="59b18-104">\[**obtener \_ Las secuencias** no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="59b18-104">\[**get\_Streams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="59b18-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="59b18-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="59b18-106">El método **Get \_ streams** crea una colección de secuencias asociadas al participante actual.</span><span class="sxs-lookup"><span data-stu-id="59b18-106">The **get\_Streams** method creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="59b18-107">Este método se proporciona para las aplicaciones cliente de automatización, como las escritas en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="59b18-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="59b18-108">Las aplicaciones de C y C++ deben usar el método [**EnumerateStreams**](itparticipant-enumeratestreams.md) .</span><span class="sxs-lookup"><span data-stu-id="59b18-108">C and C++ applications must use the [**EnumerateStreams**](itparticipant-enumeratestreams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b18-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59b18-109">Syntax</span></span>


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="59b18-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59b18-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b18-111">*pVariant* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="59b18-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59b18-112">Puntero a **Variant** que contiene un [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de punteros de la interfaz [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="59b18-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b18-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59b18-113">Return value</span></span>

<span data-ttu-id="59b18-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="59b18-114">This method can return one of these values.</span></span>



| <span data-ttu-id="59b18-115">Value</span><span class="sxs-lookup"><span data-stu-id="59b18-115">Value</span></span>                                                                                         | <span data-ttu-id="59b18-116">Significado</span><span class="sxs-lookup"><span data-stu-id="59b18-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="59b18-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="59b18-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="59b18-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="59b18-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="59b18-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="59b18-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="59b18-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="59b18-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="59b18-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="59b18-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="59b18-122">El parámetro *pVariant* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="59b18-122">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="59b18-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59b18-123">Remarks</span></span>

<span data-ttu-id="59b18-124">TAPI llama al método **AddRef** en la interfaz [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) devuelta por **ITParticipant:: get \_ streams**.</span><span class="sxs-lookup"><span data-stu-id="59b18-124">TAPI calls the **AddRef** method on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface returned by **ITParticipant::get\_Streams**.</span></span> <span data-ttu-id="59b18-125">La aplicación debe llamar a **Release** en la interfaz **ITStream** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="59b18-125">The application must call **Release** on the **ITStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b18-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59b18-126">Requirements</span></span>



| <span data-ttu-id="59b18-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b18-127">Requirement</span></span> | <span data-ttu-id="59b18-128">Value</span><span class="sxs-lookup"><span data-stu-id="59b18-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="59b18-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="59b18-129">TAPI version</span></span><br/> | <span data-ttu-id="59b18-130">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="59b18-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="59b18-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59b18-131">Header</span></span><br/>       | <dl> <span data-ttu-id="59b18-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="59b18-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="59b18-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59b18-133">Library</span></span><br/>      | <dl> <span data-ttu-id="59b18-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59b18-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="59b18-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="59b18-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="59b18-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59b18-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b18-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="59b18-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b18-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="59b18-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="59b18-139">**EnumerateStreams**</span><span class="sxs-lookup"><span data-stu-id="59b18-139">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)
</dt> <dt>

[<span data-ttu-id="59b18-140">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="59b18-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="59b18-141">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="59b18-141">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="59b18-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="59b18-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

