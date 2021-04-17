---
description: El \_ método get de velocidad de fotogramas recupera la velocidad de fotogramas de la secuencia actual. La secuencia debe ser una secuencia de vídeo.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'Método IMediaDet:: get_FrameRate (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ffabd57d85437911c323ee458d3758ee725d45a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680895"
---
# <a name="imediadetget_framerate-method"></a><span data-ttu-id="969b4-104">IMediaDet:: get \_ velocidad (método)</span><span class="sxs-lookup"><span data-stu-id="969b4-104">IMediaDet::get\_FrameRate method</span></span>

> [!Note]  
> <span data-ttu-id="969b4-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="969b4-105">\[Deprecated.</span></span> <span data-ttu-id="969b4-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="969b4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="969b4-107">El `get_FrameRate` método recupera la velocidad de fotogramas de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="969b4-107">The `get_FrameRate` method retrieves the frame rate of the current stream.</span></span> <span data-ttu-id="969b4-108">La secuencia debe ser una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="969b4-108">The stream must be a video stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="969b4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="969b4-109">Syntax</span></span>


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="969b4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="969b4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="969b4-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="969b4-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="969b4-112">Recibe la velocidad de fotogramas, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="969b4-112">Receives the frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="969b4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="969b4-113">Return value</span></span>

<span data-ttu-id="969b4-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="969b4-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="969b4-115">Entre los valores posibles figuran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="969b4-115">Possible values include the following:</span></span>



| <span data-ttu-id="969b4-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="969b4-116">Return code</span></span>                                                                                             | <span data-ttu-id="969b4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="969b4-117">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="969b4-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="969b4-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="969b4-119">El encabezado de formato de vídeo no especifica una velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="969b4-119">Video format header does not specify a frame rate.</span></span><br/> |
| <dl> <span data-ttu-id="969b4-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="969b4-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="969b4-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="969b4-121">Success.</span></span><br/>                                           |
| <dl> <span data-ttu-id="969b4-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="969b4-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="969b4-123">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="969b4-123">Invalid argument.</span></span><br/>                                  |
| <dl> <span data-ttu-id="969b4-124"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="969b4-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="969b4-125">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="969b4-125">**NULL** pointer argument.</span></span><br/>                         |
| <dl> <span data-ttu-id="969b4-126"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="969b4-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="969b4-127">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="969b4-127">Invalid media type.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="969b4-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="969b4-128">Remarks</span></span>

<span data-ttu-id="969b4-129">Este método no puede recuperar la velocidad de fotogramas de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="969b4-129">This method cannot retrieve the frame rate from an ASF file.</span></span>

<span data-ttu-id="969b4-130">Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="969b4-130">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="969b4-131">Si el detector de medios está en modo de archivo de mapa de bits, este método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="969b4-131">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="969b4-132">Para obtener más información, vea [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="969b4-132">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="969b4-133">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="969b4-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="969b4-134">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="969b4-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="969b4-135">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="969b4-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="969b4-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="969b4-136">Requirements</span></span>



| <span data-ttu-id="969b4-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="969b4-137">Requirement</span></span> | <span data-ttu-id="969b4-138">Value</span><span class="sxs-lookup"><span data-stu-id="969b4-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="969b4-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="969b4-139">Header</span></span><br/>  | <dl> <span data-ttu-id="969b4-140"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="969b4-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="969b4-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="969b4-141">Library</span></span><br/> | <dl> <span data-ttu-id="969b4-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="969b4-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="969b4-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="969b4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="969b4-144">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="969b4-144">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="969b4-145">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="969b4-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




