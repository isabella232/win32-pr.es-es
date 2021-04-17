---
description: 'El método SetDefaultFPS establece la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo. Los grupos usan este valor como la velocidad de fotogramas predeterminada. Para establecer la velocidad de fotogramas de un grupo, llame al método IAMTimelineGroup:: SetOutputFPS en el grupo.'
ms.assetid: a164f4b9-fbed-45ea-9156-cc64f0b21423
title: 'IAMTimeline:: SetDefaultFPS (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 20c352f40234672ceeb2d4c25ea9db04e89f712d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690745"
---
# <a name="iamtimelinesetdefaultfps-method"></a><span data-ttu-id="4f1ec-105">IAMTimeline:: SetDefaultFPS (método)</span><span class="sxs-lookup"><span data-stu-id="4f1ec-105">IAMTimeline::SetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="4f1ec-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-106">\[Deprecated.</span></span> <span data-ttu-id="4f1ec-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4f1ec-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4f1ec-108">El `SetDefaultFPS` método establece la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-108">The `SetDefaultFPS` method sets the default output frame rate, in frames per second.</span></span> <span data-ttu-id="4f1ec-109">Los grupos usan este valor como la velocidad de fotogramas predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-109">Groups use this value as their default frame rate.</span></span> <span data-ttu-id="4f1ec-110">Para establecer la velocidad de fotogramas de un grupo, llame al método [**IAMTimelineGroup:: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) en el grupo.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-110">To set a group's frame rate, call the [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) method on the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f1ec-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f1ec-111">Syntax</span></span>


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="4f1ec-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f1ec-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f1ec-113">*FPS*</span><span class="sxs-lookup"><span data-stu-id="4f1ec-113">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="4f1ec-114">Velocidad de fotogramas predeterminada, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-114">Default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f1ec-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f1ec-115">Return value</span></span>

<span data-ttu-id="4f1ec-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4f1ec-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f1ec-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f1ec-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f1ec-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f1ec-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4f1ec-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f1ec-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4f1ec-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4f1ec-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f1ec-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f1ec-122">Requirements</span></span>



| <span data-ttu-id="4f1ec-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f1ec-123">Requirement</span></span> | <span data-ttu-id="4f1ec-124">Value</span><span class="sxs-lookup"><span data-stu-id="4f1ec-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1ec-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f1ec-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4f1ec-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f1ec-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4f1ec-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f1ec-127">Library</span></span><br/> | <dl> <span data-ttu-id="4f1ec-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f1ec-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f1ec-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f1ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f1ec-130">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="4f1ec-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="4f1ec-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="4f1ec-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




