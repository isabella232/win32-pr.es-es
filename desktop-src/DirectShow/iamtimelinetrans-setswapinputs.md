---
description: El método SetSwapInputs especifica si se intercambian las entradas de la transición.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'IAMTimelineTrans:: SetSwapInputs (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690918"
---
# <a name="iamtimelinetranssetswapinputs-method"></a><span data-ttu-id="22034-103">IAMTimelineTrans:: SetSwapInputs (método)</span><span class="sxs-lookup"><span data-stu-id="22034-103">IAMTimelineTrans::SetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="22034-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="22034-104">\[Deprecated.</span></span> <span data-ttu-id="22034-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22034-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22034-106">El `SetSwapInputs` método especifica si se intercambian las entradas de la transición.</span><span class="sxs-lookup"><span data-stu-id="22034-106">The `SetSwapInputs` method specifies whether the transition inputs are swapped.</span></span>

<span data-ttu-id="22034-107">De forma predeterminada, una transición va desde el compuesto de todas las capas de prioridad inferior hasta la capa en la que reside la transición.</span><span class="sxs-lookup"><span data-stu-id="22034-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="22034-108">Puede invertir esta progresión, por lo que la transición va desde la capa en la que reside hasta el compuesto de capas de menor prioridad.</span><span class="sxs-lookup"><span data-stu-id="22034-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span> <span data-ttu-id="22034-109">Para obtener más información, consulte dirección de la [transición](transition-direction.md).</span><span class="sxs-lookup"><span data-stu-id="22034-109">For more information, see [Transition Direction](transition-direction.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="22034-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22034-110">Syntax</span></span>


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="22034-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22034-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22034-112">*Val*</span><span class="sxs-lookup"><span data-stu-id="22034-112">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="22034-113">Especifica si se intercambian las entradas.</span><span class="sxs-lookup"><span data-stu-id="22034-113">Specifies whether the inputs are swapped.</span></span> <span data-ttu-id="22034-114">Si **es false**, la transición va del compuesto de todas las capas de prioridad inferior a la capa de transición.</span><span class="sxs-lookup"><span data-stu-id="22034-114">If **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="22034-115">Si **es true**, la transición va en la dirección opuesta.</span><span class="sxs-lookup"><span data-stu-id="22034-115">If **TRUE**, the transition goes in the opposite direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22034-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22034-116">Return value</span></span>

<span data-ttu-id="22034-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="22034-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22034-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22034-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22034-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22034-119">Remarks</span></span>

<span data-ttu-id="22034-120">Este método no cambia la dirección del efecto visual.</span><span class="sxs-lookup"><span data-stu-id="22034-120">This method does not change the direction of the visual effect.</span></span> <span data-ttu-id="22034-121">Por ejemplo, un borrado de izquierda a derecha seguirá desplazando de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="22034-121">For example, a left-to-right wipe will still go from left to right.</span></span> <span data-ttu-id="22034-122">Para cambiar la dirección, establezca la propiedad **Progress** mediante la interfaz [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="22034-122">To change the direction, set the **Progress** property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="22034-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="22034-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="22034-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="22034-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="22034-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="22034-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22034-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22034-126">Requirements</span></span>



| <span data-ttu-id="22034-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="22034-127">Requirement</span></span> | <span data-ttu-id="22034-128">Value</span><span class="sxs-lookup"><span data-stu-id="22034-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22034-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22034-129">Header</span></span><br/>  | <dl> <span data-ttu-id="22034-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="22034-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="22034-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22034-131">Library</span></span><br/> | <dl> <span data-ttu-id="22034-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22034-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22034-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="22034-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22034-134">**Interfaz IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="22034-134">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="22034-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="22034-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




