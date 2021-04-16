---
description: El \_ método get MediaCollection obtiene un puntero a la interfaz ITMediaCollection para la Conferencia.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'Método ITSdp:: get_MediaCollection (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8812debf8c04fe022f24061660d6ea3bb5f162
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679315"
---
# <a name="itsdpget_mediacollection-method"></a><span data-ttu-id="4bf20-103">ITSdp:: get \_ MediaCollection (método)</span><span class="sxs-lookup"><span data-stu-id="4bf20-103">ITSdp::get\_MediaCollection method</span></span>

<span data-ttu-id="4bf20-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4bf20-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4bf20-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="4bf20-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4bf20-106">El método **Get \_ MediaCollection** obtiene un puntero a la interfaz [**ITMediaCollection**](itmediacollection.md) para la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="4bf20-106">The **get\_MediaCollection** method gets a pointer to the [**ITMediaCollection**](itmediacollection.md) interface for the conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf20-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bf20-107">Syntax</span></span>


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a><span data-ttu-id="4bf20-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bf20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf20-109">*ppMediaCollection* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4bf20-109">*ppMediaCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf20-110">Puntero a [**ITMediaCollection**](itmediacollection.md).</span><span class="sxs-lookup"><span data-stu-id="4bf20-110">Pointer to [**ITMediaCollection**](itmediacollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf20-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bf20-111">Return value</span></span>

<span data-ttu-id="4bf20-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="4bf20-112">This method can return one of these values.</span></span>



| <span data-ttu-id="4bf20-113">Value</span><span class="sxs-lookup"><span data-stu-id="4bf20-113">Value</span></span>                                                                                                                           | <span data-ttu-id="4bf20-114">Significado</span><span class="sxs-lookup"><span data-stu-id="4bf20-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4bf20-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4bf20-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="4bf20-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4bf20-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="4bf20-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4bf20-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="4bf20-118">El parámetro *ppMediaCollection* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="4bf20-118">The *ppMediaCollection* parameter is not a valid pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="4bf20-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4bf20-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="4bf20-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="4bf20-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="4bf20-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="4bf20-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="4bf20-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="4bf20-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="4bf20-123"><dt>**HRESULT \_ del \_ código de ERROR \_ (error de \_ datos no válidos \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="4bf20-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="4bf20-124">Se ha producido un error interno, normalmente debido a un error en un método anterior.</span><span class="sxs-lookup"><span data-stu-id="4bf20-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="4bf20-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4bf20-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="4bf20-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="4bf20-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="4bf20-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bf20-127">Remarks</span></span>

<span data-ttu-id="4bf20-128">También se puede obtener un puntero [**ITMediaCollection**](itmediacollection.md) mediante **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="4bf20-128">An [**ITMediaCollection**](itmediacollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="4bf20-129">TAPI llama al método **AddRef** en la interfaz [**ITMediaCollection**](itmediacollection.md) devuelta por **ITSdp:: get \_ MediaCollection**.</span><span class="sxs-lookup"><span data-stu-id="4bf20-129">TAPI calls the **AddRef** method on the [**ITMediaCollection**](itmediacollection.md) interface returned by **ITSdp::get\_MediaCollection**.</span></span> <span data-ttu-id="4bf20-130">La aplicación debe llamar a **Release** en la interfaz **ITMediaCollection** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="4bf20-130">The application must call **Release** on the **ITMediaCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf20-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bf20-131">Requirements</span></span>



| <span data-ttu-id="4bf20-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bf20-132">Requirement</span></span> | <span data-ttu-id="4bf20-133">Value</span><span class="sxs-lookup"><span data-stu-id="4bf20-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf20-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="4bf20-134">TAPI version</span></span><br/> | <span data-ttu-id="4bf20-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4bf20-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4bf20-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bf20-136">Header</span></span><br/>       | <dl> <span data-ttu-id="4bf20-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bf20-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4bf20-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4bf20-138">Library</span></span><br/>      | <dl> <span data-ttu-id="4bf20-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bf20-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4bf20-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4bf20-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="4bf20-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bf20-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bf20-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bf20-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf20-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="4bf20-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="4bf20-144">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="4bf20-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




