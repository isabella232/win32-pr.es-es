---
description: El \_ método get ParticipantFromSubStream permite a una aplicación detectar qué participantes están asociados a un subflujo determinado.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'Método ITParticipantSubStreamControl:: get_ParticipantFromSubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680627"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a><span data-ttu-id="8e393-103">ITParticipantSubStreamControl:: get \_ ParticipantFromSubStream (método)</span><span class="sxs-lookup"><span data-stu-id="8e393-103">ITParticipantSubStreamControl::get\_ParticipantFromSubStream method</span></span>

<span data-ttu-id="8e393-104">\[**obtener \_ ParticipantFromSubStream** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8e393-104">\[**get\_ParticipantFromSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8e393-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8e393-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8e393-106">El método **Get \_ ParticipantFromSubStream** permite a una aplicación detectar qué participantes están asociados a un subflujo determinado.</span><span class="sxs-lookup"><span data-stu-id="8e393-106">The **get\_ParticipantFromSubStream** method allows an application to discover which participants are associated with a given substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e393-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e393-107">Syntax</span></span>


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="8e393-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e393-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e393-109">*pITSubStream* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e393-109">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e393-110">Puntero a la interfaz [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="8e393-110">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8e393-111">*ppParticipant* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8e393-111">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e393-112">Puntero a la matriz de punteros de la interfaz [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="8e393-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e393-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e393-113">Return value</span></span>

<span data-ttu-id="8e393-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8e393-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8e393-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8e393-115">Return code</span></span>                                                                                     | <span data-ttu-id="8e393-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e393-116">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e393-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8e393-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="8e393-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8e393-118">Method succeeded.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="8e393-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="8e393-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="8e393-120">El parámetro *pITSubStream* o *ppParticipant* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="8e393-120">The *pITSubStream* or *ppParticipant* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="8e393-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8e393-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="8e393-122">El parámetro *pITSubStream* no apunta a una interfaz válida.</span><span class="sxs-lookup"><span data-stu-id="8e393-122">The *pITSubStream* parameter does not point to valid interface.</span></span><br/>         |
| <dl> <span data-ttu-id="8e393-123"><dt>**\_elementos TAPI E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="8e393-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="8e393-124">No hay participantes asociados a la subsecuencia.</span><span class="sxs-lookup"><span data-stu-id="8e393-124">There are no participants associated with the substream.</span></span><br/>                |
| <dl> <span data-ttu-id="8e393-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8e393-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="8e393-126">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="8e393-126">Insufficient memory exists to perform the operation.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="8e393-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e393-127">Requirements</span></span>



| <span data-ttu-id="8e393-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e393-128">Requirement</span></span> | <span data-ttu-id="8e393-129">Value</span><span class="sxs-lookup"><span data-stu-id="8e393-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e393-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8e393-130">TAPI version</span></span><br/> | <span data-ttu-id="8e393-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8e393-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8e393-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e393-132">Header</span></span><br/>       | <dl> <span data-ttu-id="8e393-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e393-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="8e393-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e393-134">Library</span></span><br/>      | <dl> <span data-ttu-id="8e393-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e393-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8e393-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e393-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="8e393-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e393-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8e393-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e393-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e393-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="8e393-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="8e393-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="8e393-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="8e393-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="8e393-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

