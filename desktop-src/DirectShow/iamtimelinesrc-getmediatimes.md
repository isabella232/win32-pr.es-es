---
description: El método GetMediaTimes recupera las horas de inicio y detención del medio.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: 'IAMTimelineSrc:: GetMediaTimes (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa6e9cbb69da504a929e23722068583489063b9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690947"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a><span data-ttu-id="3eedb-103">IAMTimelineSrc:: GetMediaTimes (método)</span><span class="sxs-lookup"><span data-stu-id="3eedb-103">IAMTimelineSrc::GetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="3eedb-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3eedb-104">\[Deprecated.</span></span> <span data-ttu-id="3eedb-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3eedb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3eedb-106">El `GetMediaTimes` método recupera las horas de inicio y detención del medio.</span><span class="sxs-lookup"><span data-stu-id="3eedb-106">The `GetMediaTimes` method retrieves the media start and stop times.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eedb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3eedb-107">Syntax</span></span>


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="3eedb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3eedb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eedb-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="3eedb-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="3eedb-110">Recibe la hora de inicio del medio, en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="3eedb-110">Receives the media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="3eedb-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="3eedb-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="3eedb-112">Recibe la hora de detención del medio, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="3eedb-112">Receives the media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eedb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3eedb-113">Return value</span></span>

<span data-ttu-id="3eedb-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3eedb-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3eedb-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3eedb-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eedb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3eedb-116">Remarks</span></span>

<span data-ttu-id="3eedb-117">Los tiempos de los medios son relativos al archivo multimedia original.</span><span class="sxs-lookup"><span data-stu-id="3eedb-117">The media times are relative to the original media file.</span></span> <span data-ttu-id="3eedb-118">Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="3eedb-118">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="3eedb-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3eedb-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3eedb-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3eedb-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3eedb-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3eedb-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3eedb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3eedb-122">Requirements</span></span>



| <span data-ttu-id="3eedb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eedb-123">Requirement</span></span> | <span data-ttu-id="3eedb-124">Value</span><span class="sxs-lookup"><span data-stu-id="3eedb-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3eedb-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3eedb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3eedb-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eedb-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3eedb-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3eedb-127">Library</span></span><br/> | <dl> <span data-ttu-id="3eedb-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3eedb-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eedb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3eedb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eedb-130">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="3eedb-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="3eedb-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="3eedb-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




