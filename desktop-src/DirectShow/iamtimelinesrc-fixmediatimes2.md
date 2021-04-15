---
description: 'El método FixMediaTimes2 redondea los valores de hora especificados al límite de fotogramas más cercano, según se define en la velocidad de fotogramas de salida. Este método es equivalente a IAMTimelineSrc:: FixMediaTimes, pero toma valores REFTIME.'
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: 'IAMTimelineSrc:: FixMediaTimes2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e38b6c1ea4c49372a52a805920fa95ccf795f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689966"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a><span data-ttu-id="12857-104">IAMTimelineSrc:: FixMediaTimes2 (método)</span><span class="sxs-lookup"><span data-stu-id="12857-104">IAMTimelineSrc::FixMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="12857-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="12857-105">\[Deprecated.</span></span> <span data-ttu-id="12857-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12857-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="12857-107">El `FixMediaTimes2` método redondea los valores de hora especificados al límite de fotogramas más cercano, según se define en la velocidad de fotogramas de salida.</span><span class="sxs-lookup"><span data-stu-id="12857-107">The `FixMediaTimes2` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="12857-108">Este método es equivalente a [**IAMTimelineSrc:: FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), pero toma valores [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="12857-108">This method is equivalent to [**IAMTimelineSrc::FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="12857-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12857-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="12857-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12857-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12857-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="12857-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="12857-112">Puntero a una variable que contiene la hora de inicio, en segundos.</span><span class="sxs-lookup"><span data-stu-id="12857-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="12857-113">Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.</span><span class="sxs-lookup"><span data-stu-id="12857-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="12857-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="12857-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="12857-115">Puntero a una variable que contiene el tiempo de detención, en segundos.</span><span class="sxs-lookup"><span data-stu-id="12857-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="12857-116">Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.</span><span class="sxs-lookup"><span data-stu-id="12857-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12857-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12857-117">Return value</span></span>

<span data-ttu-id="12857-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="12857-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12857-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="12857-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="12857-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12857-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="12857-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="12857-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="12857-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="12857-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="12857-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="12857-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="12857-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12857-124">Requirements</span></span>



| <span data-ttu-id="12857-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="12857-125">Requirement</span></span> | <span data-ttu-id="12857-126">Value</span><span class="sxs-lookup"><span data-stu-id="12857-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12857-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12857-127">Header</span></span><br/>  | <dl> <span data-ttu-id="12857-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="12857-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="12857-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12857-129">Library</span></span><br/> | <dl> <span data-ttu-id="12857-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12857-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12857-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="12857-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12857-132">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="12857-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="12857-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="12857-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




