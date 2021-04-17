---
description: 'El método SetMediaTimes2 establece las horas de detención e inicio del medio. Este método es equivalente a IAMTimelineSrc:: SetMediaTimes, pero toma valores REFTIME.'
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: 'IAMTimelineSrc:: SetMediaTimes2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4aa4f68a6fb93c329507edceea4e9665bfecd5f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690935"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a><span data-ttu-id="41789-104">IAMTimelineSrc:: SetMediaTimes2 (método)</span><span class="sxs-lookup"><span data-stu-id="41789-104">IAMTimelineSrc::SetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="41789-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="41789-105">\[Deprecated.</span></span> <span data-ttu-id="41789-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="41789-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="41789-107">El `SetMediaTimes2` método establece las horas de detención e inicio del medio.</span><span class="sxs-lookup"><span data-stu-id="41789-107">The `SetMediaTimes2` method sets the media stop and start times.</span></span> <span data-ttu-id="41789-108">Este método es equivalente a [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md), pero toma valores [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="41789-108">This method is equivalent to [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="41789-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41789-109">Syntax</span></span>


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="41789-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41789-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41789-111">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="41789-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="41789-112">Hora de inicio del medio, en segundos.</span><span class="sxs-lookup"><span data-stu-id="41789-112">Media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="41789-113">*Detención*</span><span class="sxs-lookup"><span data-stu-id="41789-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="41789-114">Tiempo de detención del medio, en segundos.</span><span class="sxs-lookup"><span data-stu-id="41789-114">Media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41789-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41789-115">Return value</span></span>

<span data-ttu-id="41789-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="41789-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41789-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41789-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41789-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41789-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="41789-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="41789-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="41789-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="41789-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="41789-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="41789-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41789-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41789-122">Requirements</span></span>



| <span data-ttu-id="41789-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="41789-123">Requirement</span></span> | <span data-ttu-id="41789-124">Value</span><span class="sxs-lookup"><span data-stu-id="41789-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41789-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41789-125">Header</span></span><br/>  | <dl> <span data-ttu-id="41789-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="41789-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="41789-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41789-127">Library</span></span><br/> | <dl> <span data-ttu-id="41789-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41789-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41789-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="41789-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41789-130">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="41789-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="41789-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="41789-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




