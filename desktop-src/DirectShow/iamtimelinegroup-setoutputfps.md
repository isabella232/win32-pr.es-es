---
description: El método SetOutputFPS establece la velocidad de fotogramas de salida sin comprimir para este grupo.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'IAMTimelineGroup:: SetOutputFPS (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690790"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a><span data-ttu-id="2c8b3-103">IAMTimelineGroup:: SetOutputFPS (método)</span><span class="sxs-lookup"><span data-stu-id="2c8b3-103">IAMTimelineGroup::SetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="2c8b3-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-104">\[Deprecated.</span></span> <span data-ttu-id="2c8b3-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2c8b3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2c8b3-106">El `SetOutputFPS` método establece la velocidad de fotogramas de salida sin comprimir para este grupo.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-106">The `SetOutputFPS` method sets the uncompressed output frame rate for this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8b3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c8b3-107">Syntax</span></span>


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="2c8b3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c8b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8b3-109">*FPS*</span><span class="sxs-lookup"><span data-stu-id="2c8b3-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="2c8b3-110">Velocidad de fotogramas de salida para este grupo, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-110">Output frame rate for this group, in frames per second.</span></span> <span data-ttu-id="2c8b3-111">El valor no puede ser igual a cero y no puede tener más de siete dígitos después de la posición decimal.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-111">The value cannot equal zero, and cannot have more than seven digits after the decimal place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8b3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c8b3-112">Return value</span></span>

<span data-ttu-id="2c8b3-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2c8b3-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2c8b3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c8b3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c8b3-115">Remarks</span></span>

<span data-ttu-id="2c8b3-116">La salida representada de este grupo se ejecuta a la velocidad de fotogramas especificada y todas las ediciones del material de origen se redondean al límite de fotogramas más cercano, según se define en la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-116">Rendered output from this group runs at the specified frame rate, and all edits on the source material are rounded to the nearest frame boundary, as defined by the frame rate.</span></span> <span data-ttu-id="2c8b3-117">Para obtener el mejor rendimiento, use la misma velocidad de fotogramas para todos los grupos, vídeo y audio.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-117">For best performance, use the same frame rate for all groups, video and audio.</span></span>

<span data-ttu-id="2c8b3-118">El método [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) sobrescribe la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-118">The [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method overwrites the frame rate.</span></span>

> [!Note]  
> <span data-ttu-id="2c8b3-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2c8b3-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2c8b3-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2c8b3-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2c8b3-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c8b3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c8b3-122">Requirements</span></span>



| <span data-ttu-id="2c8b3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c8b3-123">Requirement</span></span> | <span data-ttu-id="2c8b3-124">Value</span><span class="sxs-lookup"><span data-stu-id="2c8b3-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8b3-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c8b3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2c8b3-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c8b3-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2c8b3-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c8b3-127">Library</span></span><br/> | <dl> <span data-ttu-id="2c8b3-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c8b3-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8b3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c8b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8b3-130">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="2c8b3-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="2c8b3-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="2c8b3-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




