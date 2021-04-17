---
description: El método SetMediaType establece el tipo de medio sin comprimir para el grupo.
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'IAMTimelineGroup:: SetMediaType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a7c5366525b51367a5348bc47b9acbe0fb799db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680919"
---
# <a name="iamtimelinegroupsetmediatype-method"></a><span data-ttu-id="ffb32-103">IAMTimelineGroup:: SetMediaType (método)</span><span class="sxs-lookup"><span data-stu-id="ffb32-103">IAMTimelineGroup::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="ffb32-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="ffb32-104">\[Deprecated.</span></span> <span data-ttu-id="ffb32-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ffb32-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ffb32-106">El `SetMediaType` método establece el tipo de medio sin comprimir para el grupo.</span><span class="sxs-lookup"><span data-stu-id="ffb32-106">The `SetMediaType` method sets the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb32-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffb32-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="ffb32-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffb32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffb32-109">*pago* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ffb32-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb32-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que describe el formato.</span><span class="sxs-lookup"><span data-stu-id="ffb32-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure describing the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffb32-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffb32-111">Return value</span></span>

<span data-ttu-id="ffb32-112">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="ffb32-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="ffb32-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ffb32-113">Return code</span></span>                                                                                             | <span data-ttu-id="ffb32-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffb32-114">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="ffb32-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ffb32-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="ffb32-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="ffb32-116">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="ffb32-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="ffb32-117"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="ffb32-118">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ffb32-118">**NULL** pointer argument.</span></span><br/>           |
| <dl> <span data-ttu-id="ffb32-119"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="ffb32-119"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="ffb32-120">El tipo de medio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="ffb32-120">The specified media type is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ffb32-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffb32-121">Remarks</span></span>

<span data-ttu-id="ffb32-122">Se admiten los siguientes tipos de medios:</span><span class="sxs-lookup"><span data-stu-id="ffb32-122">The following media types are supported:</span></span>

-   <span data-ttu-id="ffb32-123">Vídeo RGB sin comprimir</span><span class="sxs-lookup"><span data-stu-id="ffb32-123">Uncompressed RGB video</span></span>
-   <span data-ttu-id="ffb32-124">16 bits por píxel, formato 555 (MEDIASUBTYPE \_ RGB555)</span><span class="sxs-lookup"><span data-stu-id="ffb32-124">16 bits per pixel, 555 format (MEDIASUBTYPE\_RGB555)</span></span>
-   <span data-ttu-id="ffb32-125">24 bits por píxel (MEDIASUBTYPE \_ RGB24)</span><span class="sxs-lookup"><span data-stu-id="ffb32-125">24 bits per pixel (MEDIASUBTYPE\_RGB24)</span></span>
-   <span data-ttu-id="ffb32-126">32 bits por píxel, con alfa (MEDIASUBTYPE \_ ARGB32, no MEDIASUBTYPE \_ RGB32)</span><span class="sxs-lookup"><span data-stu-id="ffb32-126">32 bits per pixel, with alpha (MEDIASUBTYPE\_ARGB32, not MEDIASUBTYPE\_RGB32)</span></span>
-   <span data-ttu-id="ffb32-127">audio PCM estéreo de 16 bits (MEDIASUBTYPE \_ PCM)</span><span class="sxs-lookup"><span data-stu-id="ffb32-127">16-bit stereo PCM audio (MEDIASUBTYPE\_PCM)</span></span>

<span data-ttu-id="ffb32-128">Los tipos de vídeo deben usar \_ el formato videoinfo para el tipo de formato y [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="ffb32-128">Video types must use FORMAT\_VideoInfo for the format type and [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) for the format block.</span></span> <span data-ttu-id="ffb32-129">No se admite el formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="ffb32-129">The [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format is not supported.</span></span> <span data-ttu-id="ffb32-130">Además, no se admiten los formatos de vídeo de arriba abajo (*biheight* < 0).</span><span class="sxs-lookup"><span data-stu-id="ffb32-130">Also, top-down video formats (*biHeight* < 0) are not supported.</span></span>

<span data-ttu-id="ffb32-131">Para especificar un formato de compresión para el grupo, llame al método [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) .</span><span class="sxs-lookup"><span data-stu-id="ffb32-131">To specify a compression format for the group, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="ffb32-132">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="ffb32-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ffb32-133">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ffb32-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ffb32-134">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ffb32-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ffb32-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffb32-135">Requirements</span></span>



| <span data-ttu-id="ffb32-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffb32-136">Requirement</span></span> | <span data-ttu-id="ffb32-137">Value</span><span class="sxs-lookup"><span data-stu-id="ffb32-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb32-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffb32-138">Header</span></span><br/>  | <dl> <span data-ttu-id="ffb32-139"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffb32-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ffb32-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ffb32-140">Library</span></span><br/> | <dl> <span data-ttu-id="ffb32-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffb32-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffb32-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffb32-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb32-143">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="ffb32-143">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="ffb32-144">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="ffb32-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




