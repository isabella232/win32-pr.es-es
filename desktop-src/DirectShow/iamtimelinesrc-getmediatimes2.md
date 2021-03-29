---
description: 'El método GetMediaTimes2 recupera las horas de inicio y detención del medio. Este método es equivalente a IAMTimelineSrc:: GetMediaTimes, pero toma valores REFTIME.'
ms.assetid: c3961c2c-7198-44bd-8734-7301a7c5b21e
title: 'IAMTimelineSrc:: GetMediaTimes2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 779876e542ab51914725b326a0e3b217b893f254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680573"
---
# <a name="iamtimelinesrcgetmediatimes2-method"></a><span data-ttu-id="55654-104">IAMTimelineSrc:: GetMediaTimes2 (método)</span><span class="sxs-lookup"><span data-stu-id="55654-104">IAMTimelineSrc::GetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="55654-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="55654-105">\[Deprecated.</span></span> <span data-ttu-id="55654-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="55654-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="55654-107">El `GetMediaTimes2` método recupera las horas de inicio y detención del medio.</span><span class="sxs-lookup"><span data-stu-id="55654-107">The `GetMediaTimes2` method retrieves the media start and stop times.</span></span> <span data-ttu-id="55654-108">Este método es equivalente a [**IAMTimelineSrc:: GetMediaTimes**](iamtimelinesrc-getmediatimes.md), pero toma valores [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="55654-108">This method is equivalent to [**IAMTimelineSrc::GetMediaTimes**](iamtimelinesrc-getmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="55654-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55654-109">Syntax</span></span>


```C++
HRESULT GetMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="55654-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55654-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55654-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="55654-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="55654-112">Recibe la hora de inicio del medio, en segundos.</span><span class="sxs-lookup"><span data-stu-id="55654-112">Receives the media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="55654-113">*pStop*</span><span class="sxs-lookup"><span data-stu-id="55654-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="55654-114">Recibe el tiempo de detención del medio, en segundos.</span><span class="sxs-lookup"><span data-stu-id="55654-114">Receives the media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55654-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55654-115">Return value</span></span>

<span data-ttu-id="55654-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="55654-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="55654-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="55654-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="55654-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55654-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="55654-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="55654-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="55654-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="55654-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="55654-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="55654-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="55654-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55654-122">Requirements</span></span>



| <span data-ttu-id="55654-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="55654-123">Requirement</span></span> | <span data-ttu-id="55654-124">Value</span><span class="sxs-lookup"><span data-stu-id="55654-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55654-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55654-125">Header</span></span><br/>  | <dl> <span data-ttu-id="55654-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="55654-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="55654-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55654-127">Library</span></span><br/> | <dl> <span data-ttu-id="55654-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55654-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55654-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="55654-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55654-130">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="55654-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="55654-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="55654-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




