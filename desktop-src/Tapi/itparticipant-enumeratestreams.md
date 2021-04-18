---
description: El método EnumerateStreams enumera las secuencias actualmente con los participantes. Este método se proporciona para las aplicaciones de C y C++. Las aplicaciones cliente de automatización, como las escritas en Visual Basic, deben usar el \_ método get streams.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'ITParticipant:: EnumerateStreams (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690622"
---
# <a name="itparticipantenumeratestreams-method"></a><span data-ttu-id="f6f46-105">ITParticipant:: EnumerateStreams (método)</span><span class="sxs-lookup"><span data-stu-id="f6f46-105">ITParticipant::EnumerateStreams method</span></span>

<span data-ttu-id="f6f46-106">\[**EnumerateStreams** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f6f46-106">\[**EnumerateStreams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f6f46-107">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f6f46-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f6f46-108">El método **EnumerateStreams** enumera las secuencias actualmente con los participantes.</span><span class="sxs-lookup"><span data-stu-id="f6f46-108">The **EnumerateStreams** method enumerates streams currently with the participants.</span></span> <span data-ttu-id="f6f46-109">Este método se proporciona para las aplicaciones de C y C++.</span><span class="sxs-lookup"><span data-stu-id="f6f46-109">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="f6f46-110">Las aplicaciones cliente de automatización, como las escritas en Visual Basic, deben usar el método [**Get \_ streams**](itparticipant-get-streams.md) .</span><span class="sxs-lookup"><span data-stu-id="f6f46-110">Automation client applications, such as those written in Visual Basic, must use the [**get\_Streams**](itparticipant-get-streams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f46-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6f46-111">Syntax</span></span>


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a><span data-ttu-id="f6f46-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6f46-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f46-113">*ppEnumStream* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6f46-113">*ppEnumStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6f46-114">Puntero al puntero de la interfaz [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) .</span><span class="sxs-lookup"><span data-stu-id="f6f46-114">Pointer to [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6f46-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6f46-115">Return value</span></span>

<span data-ttu-id="f6f46-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f6f46-116">This method can return one of these values.</span></span>



| <span data-ttu-id="f6f46-117">Value</span><span class="sxs-lookup"><span data-stu-id="f6f46-117">Value</span></span>                                                                                     | <span data-ttu-id="f6f46-118">Significado</span><span class="sxs-lookup"><span data-stu-id="f6f46-118">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f6f46-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f46-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="f6f46-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f6f46-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f6f46-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f46-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="f6f46-122">El parámetro *ppEnumStream* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="f6f46-122">The *ppEnumStream* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6f46-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6f46-123">Remarks</span></span>

<span data-ttu-id="f6f46-124">TAPI llama al método **AddRef** en la interfaz [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) devuelta por **ITParticipant:: EnumerateStreams**.</span><span class="sxs-lookup"><span data-stu-id="f6f46-124">TAPI calls the **AddRef** method on the [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface returned by **ITParticipant::EnumerateStreams**.</span></span> <span data-ttu-id="f6f46-125">La aplicación debe llamar a **Release** en la interfaz **IEnumStream** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="f6f46-125">The application must call **Release** on the **IEnumStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f46-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6f46-126">Requirements</span></span>



| <span data-ttu-id="f6f46-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6f46-127">Requirement</span></span> | <span data-ttu-id="f6f46-128">Value</span><span class="sxs-lookup"><span data-stu-id="f6f46-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f46-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f6f46-129">TAPI version</span></span><br/> | <span data-ttu-id="f6f46-130">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f6f46-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="f6f46-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6f46-131">Header</span></span><br/>       | <dl> <span data-ttu-id="f6f46-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f46-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6f46-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6f46-133">Library</span></span><br/>      | <dl> <span data-ttu-id="f6f46-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6f46-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="f6f46-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6f46-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="f6f46-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6f46-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6f46-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6f46-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f46-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="f6f46-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="f6f46-139">**obtener \_ secuencias**</span><span class="sxs-lookup"><span data-stu-id="f6f46-139">**get\_Streams**</span></span>](itparticipant-get-streams.md)
</dt> <dt>

[<span data-ttu-id="f6f46-140">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="f6f46-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




