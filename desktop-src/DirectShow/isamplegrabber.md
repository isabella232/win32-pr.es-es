---
description: La interfaz ISampleGrabber se expone mediante el filtro de enganche de ejemplo. Permite que una aplicación recupere muestras de medios individuales a medida que se mueven por el gráfico de filtro.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Interfaz ISampleGrabber (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678942"
---
# <a name="isamplegrabber-interface"></a><span data-ttu-id="8d36a-104">Interfaz ISampleGrabber</span><span class="sxs-lookup"><span data-stu-id="8d36a-104">ISampleGrabber interface</span></span>

> [!Note]  
> <span data-ttu-id="8d36a-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="8d36a-105">\[Deprecated.</span></span> <span data-ttu-id="8d36a-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8d36a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8d36a-107">La interfaz **ISampleGrabber** se expone mediante el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8d36a-107">The **ISampleGrabber** interface is exposed by the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="8d36a-108">Permite que una aplicación recupere muestras de medios individuales a medida que se mueven por el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="8d36a-108">It enables an application to retrieve individual media samples as they move through the filter graph.</span></span>

## <a name="members"></a><span data-ttu-id="8d36a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8d36a-109">Members</span></span>

<span data-ttu-id="8d36a-110">La interfaz **ISampleGrabber** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8d36a-110">The **ISampleGrabber** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8d36a-111">**ISampleGrabber** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8d36a-111">**ISampleGrabber** also has these types of members:</span></span>

-   [<span data-ttu-id="8d36a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8d36a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8d36a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8d36a-113">Methods</span></span>

<span data-ttu-id="8d36a-114">La interfaz **ISampleGrabber** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8d36a-114">The **ISampleGrabber** interface has these methods.</span></span>



| <span data-ttu-id="8d36a-115">Método</span><span class="sxs-lookup"><span data-stu-id="8d36a-115">Method</span></span>                                                                | <span data-ttu-id="8d36a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d36a-116">Description</span></span>                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d36a-117">**GetConnectedMediaType**</span><span class="sxs-lookup"><span data-stu-id="8d36a-117">**GetConnectedMediaType**</span></span>](isamplegrabber-getconnectedmediatype.md) | <span data-ttu-id="8d36a-118">Recupera el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8d36a-118">Retrieves the media type for the connection on the input pin of Sample Grabber.</span></span><br/>                                        |
| [<span data-ttu-id="8d36a-119">**GetCurrentBuffer**</span><span class="sxs-lookup"><span data-stu-id="8d36a-119">**GetCurrentBuffer**</span></span>](isamplegrabber-getcurrentbuffer.md)           | <span data-ttu-id="8d36a-120">Recupera una copia del ejemplo que el filtro recibió más recientemente.</span><span class="sxs-lookup"><span data-stu-id="8d36a-120">Retrieves a copy of the sample that the filter received most recently.</span></span><br/>                                                 |
| [<span data-ttu-id="8d36a-121">**GetCurrentSample**</span><span class="sxs-lookup"><span data-stu-id="8d36a-121">**GetCurrentSample**</span></span>](isamplegrabber-getcurrentsample.md)           | <span data-ttu-id="8d36a-122">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="8d36a-122">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="8d36a-123">**SetBufferSamples**</span><span class="sxs-lookup"><span data-stu-id="8d36a-123">**SetBufferSamples**</span></span>](isamplegrabber-setbuffersamples.md)           | <span data-ttu-id="8d36a-124">Especifica si se van a copiar los datos de ejemplo en un búfer a medida que pasa por el filtro.</span><span class="sxs-lookup"><span data-stu-id="8d36a-124">Specifies whether to copy sample data into a buffer as it goes through the filter.</span></span><br/>                                     |
| [<span data-ttu-id="8d36a-125">**SetCallback**</span><span class="sxs-lookup"><span data-stu-id="8d36a-125">**SetCallback**</span></span>](isamplegrabber-setcallback.md)                     | <span data-ttu-id="8d36a-126">Especifica un método de devolución de llamada al que llamar en los ejemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="8d36a-126">Specifies a callback method to call on incoming samples.</span></span><br/>                                                               |
| [<span data-ttu-id="8d36a-127">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="8d36a-127">**SetMediaType**</span></span>](isamplegrabber-setmediatype.md)                   | <span data-ttu-id="8d36a-128">Especifica el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8d36a-128">Specifies the media type for the connection on the input pin of the Sample Grabber.</span></span><br/>                                    |
| [<span data-ttu-id="8d36a-129">**SetOneShot**</span><span class="sxs-lookup"><span data-stu-id="8d36a-129">**SetOneShot**</span></span>](isamplegrabber-setoneshot.md)                       | <span data-ttu-id="8d36a-130">Especifica si el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) se detiene después de que el filtro reciba un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8d36a-130">Specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8d36a-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d36a-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8d36a-132">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="8d36a-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8d36a-133">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8d36a-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8d36a-134">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8d36a-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8d36a-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d36a-135">Requirements</span></span>



| <span data-ttu-id="8d36a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d36a-136">Requirement</span></span> | <span data-ttu-id="8d36a-137">Value</span><span class="sxs-lookup"><span data-stu-id="8d36a-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d36a-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d36a-138">Header</span></span><br/>  | <dl> <span data-ttu-id="8d36a-139"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d36a-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8d36a-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d36a-140">Library</span></span><br/> | <dl> <span data-ttu-id="8d36a-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d36a-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d36a-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d36a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d36a-143">Usar el enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d36a-143">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 
