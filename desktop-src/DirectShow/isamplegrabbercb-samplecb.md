---
description: El método SampleCB es un método de devolución de llamada que recibe un puntero al ejemplo multimedia.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'ISampleGrabberCB:: SampleCB (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e66f4a43666add7a5d6cb579fcf15f0fc1ec0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680961"
---
# <a name="isamplegrabbercbsamplecb-method"></a><span data-ttu-id="fd8d0-103">ISampleGrabberCB:: SampleCB (método)</span><span class="sxs-lookup"><span data-stu-id="fd8d0-103">ISampleGrabberCB::SampleCB method</span></span>

> [!Note]  
> <span data-ttu-id="fd8d0-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="fd8d0-104">\[Deprecated.</span></span> <span data-ttu-id="fd8d0-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fd8d0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fd8d0-106">El `SampleCB` método es un método de devolución de llamada que recibe un puntero al ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="fd8d0-106">The `SampleCB` method is a callback method that receives a pointer to the media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd8d0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd8d0-107">Syntax</span></span>


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="fd8d0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd8d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd8d0-109">*SampleTime*</span><span class="sxs-lookup"><span data-stu-id="fd8d0-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="fd8d0-110">Hora de inicio del ejemplo, en segundos.</span><span class="sxs-lookup"><span data-stu-id="fd8d0-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="fd8d0-111">*pSample*</span><span class="sxs-lookup"><span data-stu-id="fd8d0-111">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="fd8d0-112">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fd8d0-112">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd8d0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd8d0-113">Return value</span></span>

<span data-ttu-id="fd8d0-114">Devuelve S \_ correcto si se realiza correctamente o un código de error **HRESULT** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fd8d0-114">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd8d0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd8d0-115">Remarks</span></span>

<span data-ttu-id="fd8d0-116">Para configurar la devolución de llamada, llame a [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md).</span><span class="sxs-lookup"><span data-stu-id="fd8d0-116">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="fd8d0-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="fd8d0-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fd8d0-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fd8d0-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fd8d0-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fd8d0-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd8d0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd8d0-120">Requirements</span></span>



| <span data-ttu-id="fd8d0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd8d0-121">Requirement</span></span> | <span data-ttu-id="fd8d0-122">Value</span><span class="sxs-lookup"><span data-stu-id="fd8d0-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8d0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd8d0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fd8d0-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d0-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fd8d0-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd8d0-125">Library</span></span><br/> | <dl> <span data-ttu-id="fd8d0-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d0-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd8d0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd8d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8d0-128">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="fd8d0-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="fd8d0-129">**Interfaz ISampleGrabberCB**</span><span class="sxs-lookup"><span data-stu-id="fd8d0-129">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




