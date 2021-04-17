---
description: El método EffectGetPriority recupera el nivel de prioridad del efecto. Para un objeto determinado, el motor de representación aplica efectos en orden de prioridad, empezando por el nivel de prioridad cero.
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: 'IAMTimelineEffect:: EffectGetPriority (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect.EffectGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 26ea9795e3ffe36a75c354e51ff2f7e64fae40ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691080"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a><span data-ttu-id="f38ff-104">IAMTimelineEffect:: EffectGetPriority (método)</span><span class="sxs-lookup"><span data-stu-id="f38ff-104">IAMTimelineEffect::EffectGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="f38ff-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f38ff-105">\[Deprecated.</span></span> <span data-ttu-id="f38ff-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f38ff-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f38ff-107">El `EffectGetPriority` método recupera el nivel de prioridad del efecto.</span><span class="sxs-lookup"><span data-stu-id="f38ff-107">The `EffectGetPriority` method retrieves the effect's priority level.</span></span> <span data-ttu-id="f38ff-108">Para un objeto determinado, el motor de representación aplica efectos en orden de prioridad, empezando por el nivel de prioridad cero.</span><span class="sxs-lookup"><span data-stu-id="f38ff-108">For a given object, the render engine applies effects in order of priority, starting with priority level zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="f38ff-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f38ff-109">Syntax</span></span>


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f38ff-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f38ff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f38ff-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="f38ff-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f38ff-112">Recibe el nivel de prioridad.</span><span class="sxs-lookup"><span data-stu-id="f38ff-112">Receives the priority level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f38ff-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f38ff-113">Return value</span></span>

<span data-ttu-id="f38ff-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f38ff-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f38ff-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f38ff-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f38ff-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f38ff-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f38ff-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f38ff-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f38ff-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f38ff-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f38ff-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f38ff-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f38ff-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f38ff-120">Requirements</span></span>



| <span data-ttu-id="f38ff-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f38ff-121">Requirement</span></span> | <span data-ttu-id="f38ff-122">Value</span><span class="sxs-lookup"><span data-stu-id="f38ff-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f38ff-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f38ff-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f38ff-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f38ff-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f38ff-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f38ff-125">Library</span></span><br/> | <dl> <span data-ttu-id="f38ff-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f38ff-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f38ff-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f38ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38ff-128">**Interfaz IAMTimelineEffect**</span><span class="sxs-lookup"><span data-stu-id="f38ff-128">**IAMTimelineEffect Interface**</span></span>](iamtimelineeffect.md)
</dt> <dt>

[<span data-ttu-id="f38ff-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="f38ff-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




