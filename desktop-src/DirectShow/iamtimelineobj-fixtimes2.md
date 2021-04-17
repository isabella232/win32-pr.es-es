---
description: 'El método FixTimes2 redondea las horas de inicio y detención especificadas a los límites del marco más cercano, según se define en la configuración de velocidad de fotogramas del grupo primario. Este método es equivalente a IAMTimelineObj:: FixTimes, pero toma valores REFTIME.'
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'IAMTimelineObj:: FixTimes2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48b487d8dc17d6b815ea9dff79fc58af953b0bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681224"
---
# <a name="iamtimelineobjfixtimes2-method"></a><span data-ttu-id="b17d1-104">IAMTimelineObj:: FixTimes2 (método)</span><span class="sxs-lookup"><span data-stu-id="b17d1-104">IAMTimelineObj::FixTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="b17d1-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b17d1-105">\[Deprecated.</span></span> <span data-ttu-id="b17d1-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b17d1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b17d1-107">El `FixTimes2` método redondea las horas de inicio y detención especificadas a los límites del marco más cercano, según se define en la configuración de velocidad de fotogramas del grupo primario.</span><span class="sxs-lookup"><span data-stu-id="b17d1-107">The `FixTimes2` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span> <span data-ttu-id="b17d1-108">Este método es equivalente a [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md), pero toma valores [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b17d1-108">This method is equivalent to [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17d1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b17d1-109">Syntax</span></span>


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="b17d1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b17d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b17d1-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="b17d1-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b17d1-112">Puntero a una variable que contiene la hora de inicio, en segundos.</span><span class="sxs-lookup"><span data-stu-id="b17d1-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="b17d1-113">Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.</span><span class="sxs-lookup"><span data-stu-id="b17d1-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="b17d1-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="b17d1-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="b17d1-115">Puntero a una variable que contiene el tiempo de detención, en segundos.</span><span class="sxs-lookup"><span data-stu-id="b17d1-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="b17d1-116">Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.</span><span class="sxs-lookup"><span data-stu-id="b17d1-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b17d1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b17d1-117">Return value</span></span>

<span data-ttu-id="b17d1-118">Devuelve \_ si es correcto, o E \_ NOTINTREE si el objeto no forma parte de un grupo.</span><span class="sxs-lookup"><span data-stu-id="b17d1-118">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="b17d1-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b17d1-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b17d1-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b17d1-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b17d1-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b17d1-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b17d1-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b17d1-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b17d1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b17d1-123">Requirements</span></span>



| <span data-ttu-id="b17d1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17d1-124">Requirement</span></span> | <span data-ttu-id="b17d1-125">Value</span><span class="sxs-lookup"><span data-stu-id="b17d1-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b17d1-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b17d1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b17d1-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b17d1-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b17d1-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b17d1-128">Library</span></span><br/> | <dl> <span data-ttu-id="b17d1-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b17d1-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b17d1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b17d1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17d1-131">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="b17d1-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b17d1-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b17d1-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




