---
description: El método BufferCB es un método de devolución de llamada que recibe un puntero al búfer de ejemplo.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'ISampleGrabberCB:: BufferCB (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681046"
---
# <a name="isamplegrabbercbbuffercb-method"></a><span data-ttu-id="b18d2-103">ISampleGrabberCB:: BufferCB (método)</span><span class="sxs-lookup"><span data-stu-id="b18d2-103">ISampleGrabberCB::BufferCB method</span></span>

> [!Note]  
> <span data-ttu-id="b18d2-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b18d2-104">\[Deprecated.</span></span> <span data-ttu-id="b18d2-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b18d2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b18d2-106">El método **BufferCB** es un método de devolución de llamada que recibe un puntero al búfer de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b18d2-106">The **BufferCB** method is a callback method that receives a pointer to the sample buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b18d2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b18d2-107">Syntax</span></span>


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a><span data-ttu-id="b18d2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b18d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b18d2-109">*SampleTime*</span><span class="sxs-lookup"><span data-stu-id="b18d2-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="b18d2-110">Hora de inicio del ejemplo, en segundos.</span><span class="sxs-lookup"><span data-stu-id="b18d2-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="b18d2-111">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="b18d2-111">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b18d2-112">Puntero a un búfer que contiene los datos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b18d2-112">Pointer to a buffer that contains the sample data.</span></span> <span data-ttu-id="b18d2-113">El formato de los datos depende del tipo de medio del PIN de entrada del enganche de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b18d2-113">The format of the data depends on the media type of the Sample Grabber's input pin.</span></span> <span data-ttu-id="b18d2-114">Para obtener el tipo de medio, llame a [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="b18d2-114">To get the media type, call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="b18d2-115">*BufferLen*</span><span class="sxs-lookup"><span data-stu-id="b18d2-115">*BufferLen*</span></span> 
</dt> <dd>

<span data-ttu-id="b18d2-116">Longitud del búfer señalado por *pBuffer*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b18d2-116">Length of the buffer pointed to by *pBuffer*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b18d2-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b18d2-117">Return value</span></span>

<span data-ttu-id="b18d2-118">Devuelve S \_ correcto si se realiza correctamente o un código de error **HRESULT** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b18d2-118">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b18d2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b18d2-119">Remarks</span></span>

<span data-ttu-id="b18d2-120">Este método de devolución de llamada recibe un puntero a los datos en el ejemplo multimedia más reciente.</span><span class="sxs-lookup"><span data-stu-id="b18d2-120">This callback method receives a pointer to the data in the most recent media sample.</span></span>

> [!Note]  
> <span data-ttu-id="b18d2-121">Este método recibe un puntero a los datos de ejemplo originales, no una copia.</span><span class="sxs-lookup"><span data-stu-id="b18d2-121">This method receives a pointer to the original sample data, not a copy.</span></span> <span data-ttu-id="b18d2-122">La documentación original indicaba incorrectamente que *pBuffer* contiene una copia de los datos.</span><span class="sxs-lookup"><span data-stu-id="b18d2-122">The original documentation incorrectly stated that *pBuffer* contains a copy of the data.</span></span>

 

<span data-ttu-id="b18d2-123">Para configurar la devolución de llamada, llame a [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md).</span><span class="sxs-lookup"><span data-stu-id="b18d2-123">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="b18d2-124">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b18d2-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b18d2-125">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b18d2-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b18d2-126">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b18d2-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b18d2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b18d2-127">Requirements</span></span>



| <span data-ttu-id="b18d2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b18d2-128">Requirement</span></span> | <span data-ttu-id="b18d2-129">Value</span><span class="sxs-lookup"><span data-stu-id="b18d2-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b18d2-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b18d2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b18d2-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b18d2-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b18d2-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b18d2-132">Library</span></span><br/> | <dl> <span data-ttu-id="b18d2-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b18d2-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b18d2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b18d2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b18d2-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b18d2-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="b18d2-136">**Interfaz ISampleGrabberCB**</span><span class="sxs-lookup"><span data-stu-id="b18d2-136">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




