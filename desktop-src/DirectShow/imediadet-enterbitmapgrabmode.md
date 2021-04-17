---
description: El método EnterBitmapGrabMode cambia el detector de medios al modo de agarre de mapa de bits y busca el gráfico de filtro en un tiempo especificado.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'IMediaDet:: EnterBitmapGrabMode (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680231"
---
# <a name="imediadetenterbitmapgrabmode-method"></a><span data-ttu-id="37447-103">IMediaDet:: EnterBitmapGrabMode (método)</span><span class="sxs-lookup"><span data-stu-id="37447-103">IMediaDet::EnterBitmapGrabMode method</span></span>

> [!Note]  
> <span data-ttu-id="37447-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="37447-104">\[Deprecated.</span></span> <span data-ttu-id="37447-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="37447-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="37447-106">El `EnterBitmapGrabMode` método cambia el detector de medios por el modo de captura de mapa de bits y busca el gráfico de filtro en un tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="37447-106">The `EnterBitmapGrabMode` method switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="37447-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37447-107">Syntax</span></span>


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a><span data-ttu-id="37447-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37447-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37447-109">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="37447-109">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="37447-110">Tiempo, en segundos, que busca el gráfico.</span><span class="sxs-lookup"><span data-stu-id="37447-110">Time, in seconds, to which the graph seeks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37447-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37447-111">Return value</span></span>

<span data-ttu-id="37447-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="37447-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="37447-113">Entre los valores posibles figuran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="37447-113">Possible values include the following:</span></span>



| <span data-ttu-id="37447-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="37447-114">Return code</span></span>                                                                                             | <span data-ttu-id="37447-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="37447-115">Description</span></span>                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="37447-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="37447-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="37447-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="37447-117">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="37447-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="37447-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="37447-119">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="37447-119">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="37447-120"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="37447-120"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="37447-121">El archivo de origen no tiene una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="37447-121">The source file does not have a video stream.</span></span><br/> |
| <dl> <span data-ttu-id="37447-122"><dt>**\_ \_ expiró el tiempo de VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="37447-122"><dt>**VFW\_E\_TIME\_EXPIRED**</dt></span></span> </dl>    | <span data-ttu-id="37447-123">Se agotó el tiempo de espera del comando de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="37447-123">Seek command timed out.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="37447-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37447-124">Remarks</span></span>

<span data-ttu-id="37447-125">Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="37447-125">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="37447-126">Este método inserta el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) en el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="37447-126">This method inserts the [**Sample Grabber**](sample-grabber-filter.md) filter into the filter graph.</span></span> <span data-ttu-id="37447-127">Después, puede llamar a [**IMediaDet:: GetSampleGrabber**](imediadet-getsamplegrabber.md) para obtener un puntero a la interfaz [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="37447-127">You can then call [**IMediaDet::GetSampleGrabber**](imediadet-getsamplegrabber.md) to obtain a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span> <span data-ttu-id="37447-128">Una vez que el detector de medios entra en el modo de captura de mapas de bits, los distintos métodos informativos de **IMediaDet** no funcionan.</span><span class="sxs-lookup"><span data-stu-id="37447-128">Once the media detector enters bitmap grab mode, the various informational methods in **IMediaDet** do not work.</span></span>

<span data-ttu-id="37447-129">Los métodos [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md) también colocan el detector de medios en el modo de agarre de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="37447-129">The [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md) methods also put the media detector into bitmap grab mode.</span></span>

> [!Note]  
> <span data-ttu-id="37447-130">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="37447-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="37447-131">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="37447-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="37447-132">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="37447-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="37447-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37447-133">Requirements</span></span>



| <span data-ttu-id="37447-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="37447-134">Requirement</span></span> | <span data-ttu-id="37447-135">Value</span><span class="sxs-lookup"><span data-stu-id="37447-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37447-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37447-136">Header</span></span><br/>  | <dl> <span data-ttu-id="37447-137"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="37447-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="37447-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37447-138">Library</span></span><br/> | <dl> <span data-ttu-id="37447-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37447-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37447-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="37447-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37447-141">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="37447-141">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="37447-142">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="37447-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




