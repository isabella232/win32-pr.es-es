---
description: 'El método GetStartStop2 recupera las horas de inicio y detención del objeto, en relación con el elemento primario del objeto. Este método es equivalente a IAMTimelineObj:: GetStartStop, pero toma valores REFTIME.'
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'IAMTimelineObj:: GetStartStop2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690279"
---
# <a name="iamtimelineobjgetstartstop2-method"></a><span data-ttu-id="b39e7-104">IAMTimelineObj:: GetStartStop2 (método)</span><span class="sxs-lookup"><span data-stu-id="b39e7-104">IAMTimelineObj::GetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="b39e7-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b39e7-105">\[Deprecated.</span></span> <span data-ttu-id="b39e7-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b39e7-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b39e7-107">El `GetStartStop2` método recupera las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.</span><span class="sxs-lookup"><span data-stu-id="b39e7-107">The `GetStartStop2` method retrieves the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="b39e7-108">Este método es equivalente a [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md), pero toma valores [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b39e7-108">This method is equivalent to [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b39e7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b39e7-109">Syntax</span></span>


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="b39e7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b39e7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b39e7-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="b39e7-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b39e7-112">Recibe la hora de inicio, en segundos.</span><span class="sxs-lookup"><span data-stu-id="b39e7-112">Receives the start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="b39e7-113">*pStop*</span><span class="sxs-lookup"><span data-stu-id="b39e7-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="b39e7-114">Recibe el tiempo de detención, en segundos.</span><span class="sxs-lookup"><span data-stu-id="b39e7-114">Receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b39e7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b39e7-115">Return value</span></span>

<span data-ttu-id="b39e7-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b39e7-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b39e7-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b39e7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b39e7-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b39e7-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b39e7-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b39e7-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b39e7-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b39e7-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b39e7-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b39e7-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b39e7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b39e7-122">Requirements</span></span>



| <span data-ttu-id="b39e7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b39e7-123">Requirement</span></span> | <span data-ttu-id="b39e7-124">Value</span><span class="sxs-lookup"><span data-stu-id="b39e7-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b39e7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b39e7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b39e7-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b39e7-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b39e7-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b39e7-127">Library</span></span><br/> | <dl> <span data-ttu-id="b39e7-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b39e7-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b39e7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b39e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b39e7-130">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="b39e7-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b39e7-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b39e7-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




