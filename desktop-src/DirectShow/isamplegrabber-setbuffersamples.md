---
description: El método SetBufferSamples especifica si se deben copiar los datos de ejemplo en un búfer a medida que pasa por el filtro.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'ISampleGrabber:: SetBufferSamples (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680640"
---
# <a name="isamplegrabbersetbuffersamples-method"></a><span data-ttu-id="a0520-103">ISampleGrabber:: SetBufferSamples (método)</span><span class="sxs-lookup"><span data-stu-id="a0520-103">ISampleGrabber::SetBufferSamples method</span></span>

> [!Note]  
> <span data-ttu-id="a0520-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a0520-104">\[Deprecated.</span></span> <span data-ttu-id="a0520-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a0520-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a0520-106">El método **SetBufferSamples** especifica si se deben copiar los datos de ejemplo en un búfer a medida que pasa por el filtro.</span><span class="sxs-lookup"><span data-stu-id="a0520-106">The **SetBufferSamples** method specifies whether to copy sample data into a buffer as it goes through the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0520-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0520-107">Syntax</span></span>


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a><span data-ttu-id="a0520-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0520-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0520-109">*BufferThem*</span><span class="sxs-lookup"><span data-stu-id="a0520-109">*BufferThem*</span></span> 
</dt> <dd>

<span data-ttu-id="a0520-110">Valor booleano que especifica si se deben almacenar en búfer los datos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a0520-110">Boolean value specifying whether to buffer sample data.</span></span> <span data-ttu-id="a0520-111">Si **es true**, el filtro copia los datos de ejemplo en un búfer interno.</span><span class="sxs-lookup"><span data-stu-id="a0520-111">If **TRUE**, the filter copies sample data into an internal buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0520-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0520-112">Return value</span></span>

<span data-ttu-id="a0520-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a0520-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0520-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0520-114">Remarks</span></span>

<span data-ttu-id="a0520-115">Para obtener el búfer copiado, llame a [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="a0520-115">To get the copied buffer, call [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="a0520-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a0520-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a0520-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0520-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a0520-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a0520-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0520-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0520-119">Requirements</span></span>



| <span data-ttu-id="a0520-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0520-120">Requirement</span></span> | <span data-ttu-id="a0520-121">Value</span><span class="sxs-lookup"><span data-stu-id="a0520-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0520-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0520-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a0520-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0520-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a0520-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0520-124">Library</span></span><br/> | <dl> <span data-ttu-id="a0520-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0520-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0520-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0520-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0520-127">Usar el enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0520-127">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="a0520-128">**Interfaz ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="a0520-128">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




