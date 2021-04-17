---
description: El método GetSampleGrabber recupera un puntero a la interfaz ISampleGrabber, que permite que una aplicación recupere muestras individuales de una secuencia multimedia.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'IMediaDet:: GetSampleGrabber (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679535"
---
# <a name="imediadetgetsamplegrabber-method"></a><span data-ttu-id="149a7-103">IMediaDet:: GetSampleGrabber (método)</span><span class="sxs-lookup"><span data-stu-id="149a7-103">IMediaDet::GetSampleGrabber method</span></span>

> [!Note]  
> <span data-ttu-id="149a7-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="149a7-104">\[Deprecated.</span></span> <span data-ttu-id="149a7-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="149a7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="149a7-106">El `GetSampleGrabber` método recupera un puntero a la interfaz [**ISampleGrabber**](isamplegrabber.md) , que permite que una aplicación recupere muestras individuales de una secuencia multimedia.</span><span class="sxs-lookup"><span data-stu-id="149a7-106">The `GetSampleGrabber` method retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface, which enables an application to retrieve individual samples from a media stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="149a7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="149a7-107">Syntax</span></span>


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="149a7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="149a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="149a7-109">*ppVal* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="149a7-109">*ppVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="149a7-110">Recibe un puntero a la interfaz [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="149a7-110">Receives a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="149a7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="149a7-111">Return value</span></span>

<span data-ttu-id="149a7-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="149a7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="149a7-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="149a7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="149a7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="149a7-114">Remarks</span></span>

<span data-ttu-id="149a7-115">Llame a [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="149a7-115">Call [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) before calling this method.</span></span> <span data-ttu-id="149a7-116">La interfaz [**ISampleGrabber**](isamplegrabber.md) permite recuperar muestras de medios individuales de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="149a7-116">The [**ISampleGrabber**](isamplegrabber.md) interface enables you to retrieve individual media samples from the stream.</span></span> <span data-ttu-id="149a7-117">Si solo necesita un mapa de bits de un fotograma de vídeo, llame al método [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="149a7-117">If you just need a bitmap from a video frame, call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method instead.</span></span> <span data-ttu-id="149a7-118">La interfaz **ISampleGrabber** es más flexible, pero requiere más trabajo por parte de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="149a7-118">The **ISampleGrabber** interface is more flexible, but requires more work by the application.</span></span>

<span data-ttu-id="149a7-119">Si este método se ejecuta correctamente, la interfaz [**ISampleGrabber**](isamplegrabber.md) que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="149a7-119">If this method succeeds, the [**ISampleGrabber**](isamplegrabber.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="149a7-120">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="149a7-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="149a7-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="149a7-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="149a7-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="149a7-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="149a7-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="149a7-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="149a7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="149a7-124">Requirements</span></span>



| <span data-ttu-id="149a7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="149a7-125">Requirement</span></span> | <span data-ttu-id="149a7-126">Value</span><span class="sxs-lookup"><span data-stu-id="149a7-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="149a7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="149a7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="149a7-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="149a7-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="149a7-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="149a7-129">Library</span></span><br/> | <dl> <span data-ttu-id="149a7-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="149a7-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="149a7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="149a7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="149a7-132">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="149a7-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="149a7-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="149a7-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




