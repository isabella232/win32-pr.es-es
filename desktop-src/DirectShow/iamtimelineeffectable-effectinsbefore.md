---
description: El método EffectInsBefore inserta un efecto en el objeto en el nivel de prioridad especificado.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'IAMTimelineEffectable:: EffectInsBefore (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681255"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a><span data-ttu-id="e0678-103">IAMTimelineEffectable:: EffectInsBefore (método)</span><span class="sxs-lookup"><span data-stu-id="e0678-103">IAMTimelineEffectable::EffectInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="e0678-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e0678-104">\[Deprecated.</span></span> <span data-ttu-id="e0678-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e0678-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e0678-106">El `EffectInsBefore` método inserta un efecto en el objeto en el nivel de prioridad especificado.</span><span class="sxs-lookup"><span data-stu-id="e0678-106">The `EffectInsBefore` method inserts an effect into the object at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0678-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0678-107">Syntax</span></span>


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="e0678-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0678-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0678-109">*pFX*</span><span class="sxs-lookup"><span data-stu-id="e0678-109">*pFX*</span></span> 
</dt> <dd>

<span data-ttu-id="e0678-110">Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del efecto.</span><span class="sxs-lookup"><span data-stu-id="e0678-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="e0678-111">*Prioridad*</span><span class="sxs-lookup"><span data-stu-id="e0678-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="e0678-112">Nivel de prioridad en el que se va a insertar el efecto.</span><span class="sxs-lookup"><span data-stu-id="e0678-112">Priority level at which to insert the effect.</span></span> <span data-ttu-id="e0678-113">Use el valor-1 para insertar el efecto al final de la lista de prioridades.</span><span class="sxs-lookup"><span data-stu-id="e0678-113">Use the value –1 to insert the effect at the end of the priority list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0678-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0678-114">Return value</span></span>

<span data-ttu-id="e0678-115">Devuelve S \_ OK si es correcto o E \_ NOTIMPL si el objeto no es un efecto.</span><span class="sxs-lookup"><span data-stu-id="e0678-115">Returns S\_OK if successful or E\_NOTIMPL if the object is not an effect.</span></span> <span data-ttu-id="e0678-116">De lo contrario, devuelve otro valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="e0678-116">Otherwise, returns another **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0678-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0678-117">Remarks</span></span>

<span data-ttu-id="e0678-118">Las horas de inicio y detención del efecto se recortan dentro de los límites del intervalo de tiempo del objeto, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e0678-118">The start and stop times of the effect are clipped within the bounds of the object's time range, if necessary.</span></span> <span data-ttu-id="e0678-119">Si ya hay un efecto en el nivel de prioridad especificado, todos los efectos de ese punto en se mueven hacia abajo en la lista de prioridades para dejar espacio al nuevo efecto.</span><span class="sxs-lookup"><span data-stu-id="e0678-119">If there is already an effect at the specified priority level, all the effects from that point on move down the priority list to make room for the new effect.</span></span>

> [!Note]  
> <span data-ttu-id="e0678-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e0678-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e0678-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e0678-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e0678-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e0678-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e0678-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0678-123">Requirements</span></span>



| <span data-ttu-id="e0678-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0678-124">Requirement</span></span> | <span data-ttu-id="e0678-125">Value</span><span class="sxs-lookup"><span data-stu-id="e0678-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0678-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0678-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e0678-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0678-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e0678-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0678-128">Library</span></span><br/> | <dl> <span data-ttu-id="e0678-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0678-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0678-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0678-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0678-131">**Interfaz IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="e0678-131">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="e0678-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e0678-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




