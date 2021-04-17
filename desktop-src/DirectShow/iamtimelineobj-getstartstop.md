---
description: El método GetStartStop recupera las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'IAMTimelineObj:: GetStartStop (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690280"
---
# <a name="iamtimelineobjgetstartstop-method"></a><span data-ttu-id="f394b-103">IAMTimelineObj:: GetStartStop (método)</span><span class="sxs-lookup"><span data-stu-id="f394b-103">IAMTimelineObj::GetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="f394b-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f394b-104">\[Deprecated.</span></span> <span data-ttu-id="f394b-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f394b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f394b-106">El `GetStartStop` método recupera las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.</span><span class="sxs-lookup"><span data-stu-id="f394b-106">The `GetStartStop` method retrieves the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="f394b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f394b-107">Syntax</span></span>


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="f394b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f394b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f394b-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="f394b-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f394b-110">Recibe la hora de inicio, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="f394b-110">Receives the start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="f394b-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="f394b-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="f394b-112">Recibe la hora de detención, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="f394b-112">Receives the stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f394b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f394b-113">Return value</span></span>

<span data-ttu-id="f394b-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f394b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f394b-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f394b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f394b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f394b-116">Remarks</span></span>

<span data-ttu-id="f394b-117">Las composiciones, los grupos y las pistas siempre tienen una hora de inicio de 0.</span><span class="sxs-lookup"><span data-stu-id="f394b-117">Compositions, groups, and tracks always have a start time of 0.</span></span>

<span data-ttu-id="f394b-118">Durante la representación, DES redondea las horas de inicio y detención de un objeto al límite de fotogramas más cercano.</span><span class="sxs-lookup"><span data-stu-id="f394b-118">During rendering, DES rounds an object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="f394b-119">Sin embargo, DES no sobrescribe las horas del objeto.</span><span class="sxs-lookup"><span data-stu-id="f394b-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="f394b-120">Si cambia la velocidad de fotogramas de grupo, los tiempos redondeados siempre se calculan a partir de las horas originales.</span><span class="sxs-lookup"><span data-stu-id="f394b-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="f394b-121">Para obtener más información, [en servicios de edición de DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="f394b-121">For more information, [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="f394b-122">Para determinar las horas de inicio y detención en el proyecto representado, pase los valores devueltos por `GetStartStop` al método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) .</span><span class="sxs-lookup"><span data-stu-id="f394b-122">To determine the start and stop times in the rendered project, pass the values returned by `GetStartStop` to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="f394b-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f394b-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f394b-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f394b-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f394b-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f394b-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f394b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f394b-126">Requirements</span></span>



| <span data-ttu-id="f394b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f394b-127">Requirement</span></span> | <span data-ttu-id="f394b-128">Value</span><span class="sxs-lookup"><span data-stu-id="f394b-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f394b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f394b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f394b-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f394b-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f394b-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f394b-131">Library</span></span><br/> | <dl> <span data-ttu-id="f394b-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f394b-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f394b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f394b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f394b-134">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="f394b-134">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f394b-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="f394b-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




