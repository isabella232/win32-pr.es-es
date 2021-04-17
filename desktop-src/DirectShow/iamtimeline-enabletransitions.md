---
description: El método EnableTransitions habilita o deshabilita todas las transiciones de la escala de tiempo.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'IAMTimeline:: EnableTransitions (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653515"
---
# <a name="iamtimelineenabletransitions-method"></a><span data-ttu-id="b895e-103">IAMTimeline:: EnableTransitions (método)</span><span class="sxs-lookup"><span data-stu-id="b895e-103">IAMTimeline::EnableTransitions method</span></span>

> [!Note]  
> <span data-ttu-id="b895e-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b895e-104">\[Deprecated.</span></span> <span data-ttu-id="b895e-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b895e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b895e-106">El `EnableTransitions` método habilita o deshabilita todas las transiciones de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b895e-106">The `EnableTransitions` method enables or disables all transitions in the timeline.</span></span> <span data-ttu-id="b895e-107">Si se deshabilitan las transiciones, los motores de representación los tratan como cortes; es decir, la salida representada salta de forma instantánea de una pista a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="b895e-107">If transitions are disabled, the render engines treats them as cuts; that is, the rendered output jumps instantly from one track to the next.</span></span> <span data-ttu-id="b895e-108">El punto de corte predeterminado está a mitad de la duración de la transición.</span><span class="sxs-lookup"><span data-stu-id="b895e-108">The default cut point is halfway through the duration of the transition.</span></span> <span data-ttu-id="b895e-109">Puede cambiar el punto de corte llamando al método [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md) en la transición.</span><span class="sxs-lookup"><span data-stu-id="b895e-109">You can change the cut point by calling the [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md) method on the transition.</span></span> <span data-ttu-id="b895e-110">Las transiciones deshabilitadas no se quitan de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b895e-110">Disabled transitions are not removed from the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="b895e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b895e-111">Syntax</span></span>


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="b895e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b895e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b895e-113">*fEnabled*</span><span class="sxs-lookup"><span data-stu-id="b895e-113">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="b895e-114">Valor booleano que especifica si se van a habilitar o deshabilitar las transiciones.</span><span class="sxs-lookup"><span data-stu-id="b895e-114">Boolean value that specifies whether to enable or disable transitions.</span></span> <span data-ttu-id="b895e-115">Si **es true**, las transiciones están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="b895e-115">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="b895e-116">Si **es false**, las transiciones están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="b895e-116">If **FALSE**, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b895e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b895e-117">Return value</span></span>

<span data-ttu-id="b895e-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b895e-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b895e-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b895e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b895e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b895e-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b895e-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b895e-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b895e-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b895e-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b895e-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b895e-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b895e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b895e-124">Requirements</span></span>



| <span data-ttu-id="b895e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b895e-125">Requirement</span></span> | <span data-ttu-id="b895e-126">Value</span><span class="sxs-lookup"><span data-stu-id="b895e-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b895e-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b895e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b895e-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b895e-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b895e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b895e-129">Library</span></span><br/> | <dl> <span data-ttu-id="b895e-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b895e-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b895e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b895e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b895e-132">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="b895e-132">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="b895e-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b895e-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




