---
description: El método SetCutsOnly especifica si la transición se representa como un corte. Si es así, la transición se produce al instante en el punto de corte. Si una transición tarda mucho tiempo en representarse, puede que desee obtener una vista previa de la vista previa de la velocidad.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'IAMTimelineTrans:: SetCutsOnly (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691098"
---
# <a name="iamtimelinetranssetcutsonly-method"></a><span data-ttu-id="ddf00-105">IAMTimelineTrans:: SetCutsOnly (método)</span><span class="sxs-lookup"><span data-stu-id="ddf00-105">IAMTimelineTrans::SetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="ddf00-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="ddf00-106">\[Deprecated.</span></span> <span data-ttu-id="ddf00-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ddf00-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ddf00-108">El `SetCutsOnly` método especifica si la transición se representa como un corte.</span><span class="sxs-lookup"><span data-stu-id="ddf00-108">The `SetCutsOnly` method specifies whether the transition is rendered as a cut.</span></span> <span data-ttu-id="ddf00-109">Si es así, la transición se produce al instante en el punto de corte.</span><span class="sxs-lookup"><span data-stu-id="ddf00-109">If so, the transition occurs instantly at the cut point.</span></span> <span data-ttu-id="ddf00-110">Si una transición tarda mucho tiempo en representarse, puede que desee obtener una vista previa de la vista previa de la velocidad.</span><span class="sxs-lookup"><span data-stu-id="ddf00-110">If a transition takes a long time to render, you might want to preview it as a cut to speed preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddf00-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddf00-111">Syntax</span></span>


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="ddf00-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddf00-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddf00-113">*Val*</span><span class="sxs-lookup"><span data-stu-id="ddf00-113">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="ddf00-114">Especifica si se va a representar la transición como un corte.</span><span class="sxs-lookup"><span data-stu-id="ddf00-114">Specifies whether to render the transition as a cut.</span></span> <span data-ttu-id="ddf00-115">Si es **true**, la transición se representa como un corte instantáneo.</span><span class="sxs-lookup"><span data-stu-id="ddf00-115">If **TRUE**, the transition is rendered as an instantaneous cut.</span></span> <span data-ttu-id="ddf00-116">Si **es false**, la transición se representa a lo largo de su duración normal.</span><span class="sxs-lookup"><span data-stu-id="ddf00-116">If **FALSE**, the transition renders over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddf00-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddf00-117">Return value</span></span>

<span data-ttu-id="ddf00-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ddf00-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ddf00-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ddf00-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddf00-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddf00-120">Remarks</span></span>

<span data-ttu-id="ddf00-121">La representación de una transición como un corte no es compatible con el intercambio de las entradas.</span><span class="sxs-lookup"><span data-stu-id="ddf00-121">Rendering a transition as a cut is not compatible with swapping the inputs.</span></span> <span data-ttu-id="ddf00-122">(Vea [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md)). Si se llama a `SetCutsOnly` con un valor de **true**, se invalida temporalmente el valor de **SetSwapInputs** .</span><span class="sxs-lookup"><span data-stu-id="ddf00-122">(See [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) If you call `SetCutsOnly` with a value of **TRUE**, it temporarily overrides the **SetSwapInputs** setting.</span></span> <span data-ttu-id="ddf00-123">La configuración de solo cortes está pensada para la vista previa, sin embargo, por lo que esta limitación no afecta a la salida del archivo, simplemente Recuerde llamar a `SetCutsOnly` con el valor **false** antes de escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="ddf00-123">The cuts-only setting is intended for preview, however, so this limitation does not affect file output—just remember to call `SetCutsOnly` with the value **FALSE** before writing the file.</span></span>

> [!Note]  
> <span data-ttu-id="ddf00-124">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="ddf00-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ddf00-125">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ddf00-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ddf00-126">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ddf00-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ddf00-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddf00-127">Requirements</span></span>



| <span data-ttu-id="ddf00-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddf00-128">Requirement</span></span> | <span data-ttu-id="ddf00-129">Value</span><span class="sxs-lookup"><span data-stu-id="ddf00-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf00-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddf00-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ddf00-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf00-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ddf00-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ddf00-132">Library</span></span><br/> | <dl> <span data-ttu-id="ddf00-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddf00-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddf00-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddf00-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf00-135">**Interfaz IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="ddf00-135">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="ddf00-136">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="ddf00-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




