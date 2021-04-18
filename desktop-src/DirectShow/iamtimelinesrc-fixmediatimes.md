---
description: El método FixMediaTimes redondea los valores de hora especificados al límite de fotogramas más cercano, según se define en la velocidad de fotogramas de salida. En general, las aplicaciones no necesitan llamar a este método.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'IAMTimelineSrc:: FixMediaTimes (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689967"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a><span data-ttu-id="0210c-104">IAMTimelineSrc:: FixMediaTimes (método)</span><span class="sxs-lookup"><span data-stu-id="0210c-104">IAMTimelineSrc::FixMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="0210c-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="0210c-105">\[Deprecated.</span></span> <span data-ttu-id="0210c-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0210c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0210c-107">El `FixMediaTimes` método redondea los valores de hora especificados al límite de fotogramas más cercano, según se define en la velocidad de fotogramas de salida.</span><span class="sxs-lookup"><span data-stu-id="0210c-107">The `FixMediaTimes` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="0210c-108">En general, las aplicaciones no necesitan llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="0210c-108">In general, applications do not need to call this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0210c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0210c-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="0210c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0210c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0210c-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="0210c-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="0210c-112">Puntero a una variable que contiene la hora de inicio, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="0210c-112">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="0210c-113">Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.</span><span class="sxs-lookup"><span data-stu-id="0210c-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="0210c-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="0210c-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="0210c-115">Puntero a una variable que contiene la hora de detención, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="0210c-115">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="0210c-116">Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.</span><span class="sxs-lookup"><span data-stu-id="0210c-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0210c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0210c-117">Return value</span></span>

<span data-ttu-id="0210c-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0210c-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0210c-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0210c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0210c-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0210c-120">Remarks</span></span>

<span data-ttu-id="0210c-121">Este método es similar al método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) , pero conserva la relación original de las horas de los medios y los tiempos de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0210c-121">This method is similar to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method, but it preserves the original ratio of media times and timeline times.</span></span> <span data-ttu-id="0210c-122">Simplemente redondear las horas al límite de fotogramas más cercano podría distorsionar esta relación.</span><span class="sxs-lookup"><span data-stu-id="0210c-122">Just rounding the times to the nearest frame boundary could distort this ratio.</span></span>

> [!Note]  
> <span data-ttu-id="0210c-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="0210c-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0210c-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0210c-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0210c-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0210c-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0210c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0210c-126">Requirements</span></span>



| <span data-ttu-id="0210c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0210c-127">Requirement</span></span> | <span data-ttu-id="0210c-128">Value</span><span class="sxs-lookup"><span data-stu-id="0210c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0210c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0210c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0210c-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="0210c-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0210c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0210c-131">Library</span></span><br/> | <dl> <span data-ttu-id="0210c-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0210c-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0210c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0210c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0210c-134">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="0210c-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="0210c-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="0210c-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




