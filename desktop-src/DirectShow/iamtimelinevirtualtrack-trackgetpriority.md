---
description: El método TrackGetPriority recupera el nivel de prioridad del objeto.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: 'IAMTimelineVirtualTrack:: TrackGetPriority (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08b43fa34848e5dac41d22281c08d25ee9065831
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690858"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a><span data-ttu-id="f29e8-103">IAMTimelineVirtualTrack:: TrackGetPriority (método)</span><span class="sxs-lookup"><span data-stu-id="f29e8-103">IAMTimelineVirtualTrack::TrackGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="f29e8-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f29e8-104">\[Deprecated.</span></span> <span data-ttu-id="f29e8-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f29e8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f29e8-106">El `TrackGetPriority` método recupera el nivel de prioridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="f29e8-106">The `TrackGetPriority` method retrieves the object's priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="f29e8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f29e8-107">Syntax</span></span>


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="f29e8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f29e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f29e8-109">*pPriority*</span><span class="sxs-lookup"><span data-stu-id="f29e8-109">*pPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="f29e8-110">Puntero a una variable que recibe el nivel de prioridad.</span><span class="sxs-lookup"><span data-stu-id="f29e8-110">Pointer to a variable that receives the priority level.</span></span> <span data-ttu-id="f29e8-111">Si el objeto no forma parte de una escala de tiempo, el valor se establece en – 1.</span><span class="sxs-lookup"><span data-stu-id="f29e8-111">If the object is not part of a timeline, the value is set to –1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f29e8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f29e8-112">Return value</span></span>

<span data-ttu-id="f29e8-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f29e8-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f29e8-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f29e8-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f29e8-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f29e8-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f29e8-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f29e8-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f29e8-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f29e8-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f29e8-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f29e8-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f29e8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f29e8-119">Requirements</span></span>



| <span data-ttu-id="f29e8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f29e8-120">Requirement</span></span> | <span data-ttu-id="f29e8-121">Value</span><span class="sxs-lookup"><span data-stu-id="f29e8-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f29e8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f29e8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f29e8-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f29e8-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f29e8-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f29e8-124">Library</span></span><br/> | <dl> <span data-ttu-id="f29e8-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f29e8-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f29e8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f29e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29e8-127">**Interfaz IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="f29e8-127">**IAMTimelineVirtualTrack Interface**</span></span>](iamtimelinevirtualtrack.md)
</dt> <dt>

[<span data-ttu-id="f29e8-128">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="f29e8-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




