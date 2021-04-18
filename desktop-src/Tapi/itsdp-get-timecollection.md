---
description: El \_ método get TimeCollection obtiene un puntero a una interfaz ITTimeCollection para la Conferencia.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'Método ITSdp:: get_TimeCollection (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690645"
---
# <a name="itsdpget_timecollection-method"></a><span data-ttu-id="5df17-103">ITSdp:: get \_ TimeCollection (método)</span><span class="sxs-lookup"><span data-stu-id="5df17-103">ITSdp::get\_TimeCollection method</span></span>

<span data-ttu-id="5df17-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5df17-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5df17-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="5df17-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5df17-106">El método **Get \_ TimeCollection** obtiene un puntero a una interfaz [**ITTimeCollection**](ittimecollection.md) para la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="5df17-106">The **get\_TimeCollection** method gets a pointer to an [**ITTimeCollection**](ittimecollection.md) interface for conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df17-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5df17-107">Syntax</span></span>


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a><span data-ttu-id="5df17-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5df17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df17-109">*ppTimeCollection* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5df17-109">*ppTimeCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5df17-110">Puntero a [**ITTimeCollection**](ittimecollection.md).</span><span class="sxs-lookup"><span data-stu-id="5df17-110">Pointer to [**ITTimeCollection**](ittimecollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5df17-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5df17-111">Return value</span></span>

<span data-ttu-id="5df17-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="5df17-112">This method can return one of these values.</span></span>



| <span data-ttu-id="5df17-113">Value</span><span class="sxs-lookup"><span data-stu-id="5df17-113">Value</span></span>                                                                                                                           | <span data-ttu-id="5df17-114">Significado</span><span class="sxs-lookup"><span data-stu-id="5df17-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5df17-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5df17-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="5df17-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5df17-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="5df17-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5df17-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="5df17-118">El parámetro *ppTimeCollection* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="5df17-118">The *ppTimeCollection* parameter is not a valid pointer.</span></span><br/>                         |
| <dl> <span data-ttu-id="5df17-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5df17-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="5df17-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="5df17-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="5df17-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="5df17-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="5df17-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="5df17-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="5df17-123"><dt>**HRESULT \_ del \_ código de ERROR \_ (error de \_ datos no válidos \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="5df17-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="5df17-124">Se ha producido un error interno, normalmente debido a un error en un método anterior.</span><span class="sxs-lookup"><span data-stu-id="5df17-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="5df17-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="5df17-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="5df17-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="5df17-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="5df17-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5df17-127">Remarks</span></span>

<span data-ttu-id="5df17-128">También se puede obtener un puntero [**ITTimeCollection**](ittimecollection.md) mediante **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="5df17-128">An [**ITTimeCollection**](ittimecollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="5df17-129">TAPI llama al método **AddRef** en la interfaz [**ITTimeCollection**](ittimecollection.md) devuelta por **ITSdp:: get \_ TimeCollection**.</span><span class="sxs-lookup"><span data-stu-id="5df17-129">TAPI calls the **AddRef** method on the [**ITTimeCollection**](ittimecollection.md) interface returned by **ITSdp::get\_TimeCollection**.</span></span> <span data-ttu-id="5df17-130">La aplicación debe llamar a **Release** en la interfaz **ITTimeCollection** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="5df17-130">The application must call **Release** on the **ITTimeCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df17-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5df17-131">Requirements</span></span>



| <span data-ttu-id="5df17-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5df17-132">Requirement</span></span> | <span data-ttu-id="5df17-133">Value</span><span class="sxs-lookup"><span data-stu-id="5df17-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5df17-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="5df17-134">TAPI version</span></span><br/> | <span data-ttu-id="5df17-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5df17-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5df17-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5df17-136">Header</span></span><br/>       | <dl> <span data-ttu-id="5df17-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5df17-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5df17-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5df17-138">Library</span></span><br/>      | <dl> <span data-ttu-id="5df17-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5df17-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5df17-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5df17-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="5df17-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5df17-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5df17-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="5df17-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df17-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="5df17-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="5df17-144">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="5df17-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> </dl>

 

 




