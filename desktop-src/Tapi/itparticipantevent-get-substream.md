---
description: El \_ subflujo Get obtiene un puntero a una matriz de interfaces ITSubStream que representan las subsecuencias implicadas en el evento.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'Método ITParticipantEvent:: get_SubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690490"
---
# <a name="itparticipanteventget_substream-method"></a><span data-ttu-id="bc716-103">ITParticipantEvent:: get ( \_ método de subsecuencia)</span><span class="sxs-lookup"><span data-stu-id="bc716-103">ITParticipantEvent::get\_SubStream method</span></span>

<span data-ttu-id="bc716-104">\[**obtener \_ La subsecuencia** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bc716-104">\[**get\_SubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bc716-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="bc716-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bc716-106">El **\_ subflujo Get** obtiene un puntero a una matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representan las subsecuencias implicadas en el evento.</span><span class="sxs-lookup"><span data-stu-id="bc716-106">The **get\_SubStream** gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc716-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc716-107">Syntax</span></span>


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="bc716-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc716-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc716-109">*ppSubStream* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bc716-109">*ppSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc716-110">Puntero a una matriz de punteros [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="bc716-110">Pointer to array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc716-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc716-111">Return value</span></span>

<span data-ttu-id="bc716-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="bc716-112">This method can return one of these values.</span></span>



| <span data-ttu-id="bc716-113">Value</span><span class="sxs-lookup"><span data-stu-id="bc716-113">Value</span></span>                                                                                           | <span data-ttu-id="bc716-114">Significado</span><span class="sxs-lookup"><span data-stu-id="bc716-114">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bc716-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bc716-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="bc716-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bc716-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bc716-117"><dt>**\_elementos TAPI E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="bc716-117"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="bc716-118">No hay subsecuencias asociadas al evento.</span><span class="sxs-lookup"><span data-stu-id="bc716-118">There are no substreams associated with the event.</span></span><br/>   |
| <dl> <span data-ttu-id="bc716-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bc716-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="bc716-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="bc716-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bc716-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="bc716-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="bc716-122">El parámetro *ppSubStream* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="bc716-122">The *ppSubStream* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="bc716-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc716-123">Requirements</span></span>



| <span data-ttu-id="bc716-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc716-124">Requirement</span></span> | <span data-ttu-id="bc716-125">Value</span><span class="sxs-lookup"><span data-stu-id="bc716-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc716-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="bc716-126">TAPI version</span></span><br/> | <span data-ttu-id="bc716-127">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="bc716-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bc716-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc716-128">Header</span></span><br/>       | <dl> <span data-ttu-id="bc716-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc716-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="bc716-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc716-130">Library</span></span><br/>      | <dl> <span data-ttu-id="bc716-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc716-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bc716-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc716-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="bc716-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc716-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bc716-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc716-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc716-135">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="bc716-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="bc716-136">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="bc716-136">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

