---
description: El \_ método get SubStreamFromParticipant permite a una aplicación detectar qué subsecuencias están asociadas a un participante determinado.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'Método ITParticipantSubStreamControl:: get_SubStreamFromParticipant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681243"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a><span data-ttu-id="0b253-103">ITParticipantSubStreamControl:: get \_ SubStreamFromParticipant (método)</span><span class="sxs-lookup"><span data-stu-id="0b253-103">ITParticipantSubStreamControl::get\_SubStreamFromParticipant method</span></span>

<span data-ttu-id="0b253-104">\[**obtener \_ SubStreamFromParticipant** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0b253-104">\[**get\_SubStreamFromParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0b253-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0b253-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0b253-106">El método **Get \_ SubStreamFromParticipant** permite a una aplicación detectar qué subsecuencias están asociadas a un participante determinado.</span><span class="sxs-lookup"><span data-stu-id="0b253-106">The **get\_SubStreamFromParticipant** method allows an application to discover which substreams are associated with a given participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b253-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b253-107">Syntax</span></span>


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="0b253-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b253-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b253-109">*pParticipant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b253-109">*pParticipant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b253-110">Puntero a la interfaz [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="0b253-110">Pointer to [**ITParticipant**](itparticipant.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0b253-111">*ppITSubStream* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0b253-111">*ppITSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b253-112">Puntero a la matriz de punteros de la interfaz [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="0b253-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b253-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b253-113">Return value</span></span>

<span data-ttu-id="0b253-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0b253-114">This method can return one of these values.</span></span>



| <span data-ttu-id="0b253-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0b253-115">Return code</span></span>                                                                                   | <span data-ttu-id="0b253-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b253-116">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b253-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0b253-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0b253-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b253-118">Method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="0b253-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0b253-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0b253-120">El parámetro *ppITSubStream* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="0b253-120">The *ppITSubStream* parameter is not a valid pointer.</span></span><br/>             |
| <dl> <span data-ttu-id="0b253-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0b253-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0b253-122">El parámetro *pParticipant* no apunta a una interfaz válida.</span><span class="sxs-lookup"><span data-stu-id="0b253-122">The *pParticipant* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="0b253-123"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="0b253-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="0b253-124">No se pudo obtener acceso a la información del participante de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0b253-124">The stream's participant information could not be accessed.</span></span><br/>       |
| <dl> <span data-ttu-id="0b253-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0b253-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0b253-126">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="0b253-126">Insufficient memory exists to perform the operation.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="0b253-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b253-127">Requirements</span></span>



| <span data-ttu-id="0b253-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b253-128">Requirement</span></span> | <span data-ttu-id="0b253-129">Value</span><span class="sxs-lookup"><span data-stu-id="0b253-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b253-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="0b253-130">TAPI version</span></span><br/> | <span data-ttu-id="0b253-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0b253-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0b253-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b253-132">Header</span></span><br/>       | <dl> <span data-ttu-id="0b253-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b253-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="0b253-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b253-134">Library</span></span><br/>      | <dl> <span data-ttu-id="0b253-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b253-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0b253-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b253-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="0b253-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b253-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0b253-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b253-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b253-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="0b253-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="0b253-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="0b253-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="0b253-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="0b253-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

