---
title: El valor de enumeración D1115 no es válido
description: El valor de enumeración D1115 no es válido
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- Valor de enumeración D1115 no válido Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105650255"
---
# <a name="d1115-enumeration-value-not-valid"></a><span data-ttu-id="7b0e3-104">D1115: el valor de enumeración no es válido</span><span class="sxs-lookup"><span data-stu-id="7b0e3-104">D1115: Enumeration Value Not Valid</span></span>

<span data-ttu-id="7b0e3-105">El parámetro de parámetro \[  \] con \[ *valor* \] de valor para *interface*::*Method* no es un valor de enumeración válido.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-105">The parameter \[*parameter*\] with value \[*value*\] for *interface*::*method* is not a valid enumeration value.</span></span>

## <a name="placeholders"></a><span data-ttu-id="7b0e3-106">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="7b0e3-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="7b0e3-107"><span id="parameter"></span><span id="PARAMETER"></span>*parámetro*</span><span class="sxs-lookup"><span data-stu-id="7b0e3-107"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="7b0e3-108">Nombre del parámetro que recibió el tipo inesperado.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-108">The name of the parameter that received the unexpected type.</span></span>

</dd> <dt>

<span data-ttu-id="7b0e3-109"><span id="value"></span><span id="VALUE"></span>*valor*</span><span class="sxs-lookup"><span data-stu-id="7b0e3-109"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="7b0e3-110">Valor de enumeración no válido.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-110">The invalid enumeration value.</span></span>

</dd> <dt>

<span data-ttu-id="7b0e3-111"><span id="interface"></span><span id="INTERFACE"></span>*interfaz*</span><span class="sxs-lookup"><span data-stu-id="7b0e3-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="7b0e3-112">Nombre de la interfaz a la que pertenece el *método* .</span><span class="sxs-lookup"><span data-stu-id="7b0e3-112">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="7b0e3-113"><span id="method"></span><span id="METHOD"></span>*forma*</span><span class="sxs-lookup"><span data-stu-id="7b0e3-113"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="7b0e3-114">Nombre del método que recibió el valor de enumeración no válido.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-114">The name of the method that received the invalid enumeration value.</span></span>

</dd> </dl> 




 

## <a name="examples"></a><span data-ttu-id="7b0e3-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7b0e3-115">Examples</span></span>

<span data-ttu-id="7b0e3-116">En el ejemplo siguiente se especifica un valor de enumeración de tipo de destino de representación de D2D1 de 30, que está fuera del intervalo esperado. [**\_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)</span><span class="sxs-lookup"><span data-stu-id="7b0e3-116">The following example specifies a [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) enumeration value of 30, which is outside the expected range.</span></span>


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



<span data-ttu-id="7b0e3-117">Este ejemplo genera el siguiente mensaje de depuración:</span><span class="sxs-lookup"><span data-stu-id="7b0e3-117">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a><span data-ttu-id="7b0e3-118">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="7b0e3-118">Possible Causes</span></span>

<span data-ttu-id="7b0e3-119">Un parámetro usó un valor de enumeración no válido.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-119">A parameter used an invalid enumeration value.</span></span>

## <a name="fixes"></a><span data-ttu-id="7b0e3-120">Correcciones</span><span class="sxs-lookup"><span data-stu-id="7b0e3-120">Fixes</span></span>

<span data-ttu-id="7b0e3-121">Use un valor de enumeración válido.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-121">Use a valid enumeration value.</span></span>

> [!Note]  
> <span data-ttu-id="7b0e3-122">La capa de depuración solo comprueba actualmente los valores de enumeración individuales; no comprueba si una combinación bit a bit es válida.</span><span class="sxs-lookup"><span data-stu-id="7b0e3-122">The debug layer currently checks only the individual enumeration values; it does not check whether a bitwise combination is valid.</span></span>

 

 

 
