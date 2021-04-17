---
description: El \_ método put AlphaRamp especifica la propiedad de rampa alfa. La rampa alfa es el porcentaje por el que se ajustan los valores alfa de la imagen original. Por ejemplo, si la rampa alfa es 0,5, los valores alfa de la imagen se reducen al 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: 'IDxtAlphaSetter: método de ut_AlphaRamp de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691042"
---
# <a name="idxtalphasetterput_alpharamp-method"></a><span data-ttu-id="d07a0-105">IDxtAlphaSetter::p \_ método AlphaRamp UT</span><span class="sxs-lookup"><span data-stu-id="d07a0-105">IDxtAlphaSetter::put\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="d07a0-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d07a0-106">\[Deprecated.</span></span> <span data-ttu-id="d07a0-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d07a0-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d07a0-108">El `put_AlphaRamp` método especifica la propiedad de rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="d07a0-108">The `put_AlphaRamp` method specifies the alpha ramp property.</span></span> <span data-ttu-id="d07a0-109">La rampa alfa es el porcentaje por el que se ajustan los valores alfa de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="d07a0-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="d07a0-110">Por ejemplo, si la rampa alfa es 0,5, los valores alfa de la imagen se reducen al 50%.</span><span class="sxs-lookup"><span data-stu-id="d07a0-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="d07a0-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d07a0-111">Syntax</span></span>


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="d07a0-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d07a0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d07a0-113">*Alfa* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d07a0-113">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d07a0-114">La rampa alfa como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="d07a0-114">The alpha ramp as a percentage.</span></span> <span data-ttu-id="d07a0-115">Por ejemplo, 1,0 es 100%.</span><span class="sxs-lookup"><span data-stu-id="d07a0-115">For example, 1.0 is 100%.</span></span> <span data-ttu-id="d07a0-116">Para deshabilitar esta propiedad, establezca un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="d07a0-116">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d07a0-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d07a0-117">Return value</span></span>

<span data-ttu-id="d07a0-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d07a0-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d07a0-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d07a0-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d07a0-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d07a0-120">Remarks</span></span>

<span data-ttu-id="d07a0-121">Si establece esta propiedad en un valor no negativo, también debe deshabilitar la propiedad alfa llamando a **Put \_ Alpha** con un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="d07a0-121">If you set this property to a non-negative value, you must also disable the alpha property, by calling **put\_Alpha** with a negative value.</span></span> <span data-ttu-id="d07a0-122">De lo contrario, el efecto no se representará correctamente.</span><span class="sxs-lookup"><span data-stu-id="d07a0-122">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="d07a0-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d07a0-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d07a0-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d07a0-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d07a0-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d07a0-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d07a0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d07a0-126">Requirements</span></span>



| <span data-ttu-id="d07a0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d07a0-127">Requirement</span></span> | <span data-ttu-id="d07a0-128">Value</span><span class="sxs-lookup"><span data-stu-id="d07a0-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d07a0-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d07a0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d07a0-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d07a0-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d07a0-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d07a0-131">Library</span></span><br/> | <dl> <span data-ttu-id="d07a0-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d07a0-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d07a0-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d07a0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d07a0-134">**Interfaz IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="d07a0-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="d07a0-135">**IDxtAlphaSetter::p el \_ alfa de UT**</span><span class="sxs-lookup"><span data-stu-id="d07a0-135">**IDxtAlphaSetter::put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




