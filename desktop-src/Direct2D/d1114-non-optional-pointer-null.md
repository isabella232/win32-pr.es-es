---
title: D1114 puntero no opcional nulo
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: 'El parámetro de la interfaz:: Method no es opcional. Se pasó un puntero nulo. Esto hará que se bloquee Direct2D.'
keywords:
- D1114 un puntero no opcional NULL Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105650229"
---
# <a name="d1114-non-optional-pointer-null"></a><span data-ttu-id="fec16-106">D1114: puntero nulo no opcional</span><span class="sxs-lookup"><span data-stu-id="fec16-106">D1114: Non Optional Pointer NULL</span></span>

<span data-ttu-id="fec16-107">El \[ *parámetro* Parameter \] para *interface*::*Method* no es opcional.</span><span class="sxs-lookup"><span data-stu-id="fec16-107">The parameter \[*parameter*\] for *interface*::*method* is not optional.</span></span> <span data-ttu-id="fec16-108">Se pasó un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="fec16-108">A **NULL** pointer was passed.</span></span> <span data-ttu-id="fec16-109">Esto hará que se bloquee Direct2D.</span><span class="sxs-lookup"><span data-stu-id="fec16-109">This will cause Direct2D to crash.</span></span>

### <a name="placeholders"></a><span data-ttu-id="fec16-110">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="fec16-110">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="fec16-111"><span id="parameter"></span><span id="PARAMETER"></span>*parámetro*</span><span class="sxs-lookup"><span data-stu-id="fec16-111"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="fec16-112">Nombre del parámetro que contiene el puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="fec16-112">The name of the parameter that contains the **NULL** pointer.</span></span>

</dd> <dt>

<span data-ttu-id="fec16-113"><span id="interface"></span><span id="INTERFACE"></span>*interfaz*</span><span class="sxs-lookup"><span data-stu-id="fec16-113"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="fec16-114">Nombre de la interfaz a la que pertenece el *método* .</span><span class="sxs-lookup"><span data-stu-id="fec16-114">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="fec16-115"><span id="method"></span><span id="METHOD"></span>*forma*</span><span class="sxs-lookup"><span data-stu-id="fec16-115"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="fec16-116">Nombre del método que recibió el parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="fec16-116">The name of the method that received the invalid parameter.</span></span>

</dd> </dl> 




 

### <a name="examples"></a><span data-ttu-id="fec16-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fec16-117">Examples</span></span>

<span data-ttu-id="fec16-118">En el ejemplo siguiente se muestra que el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) recibe un puntero NULL para el parámetro *Geometry* no opcional.</span><span class="sxs-lookup"><span data-stu-id="fec16-118">The following example shows that the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method receives a NULL pointer for the non-optional *geometry* parameter.</span></span>


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



<span data-ttu-id="fec16-119">Este ejemplo genera el siguiente mensaje de depuración:</span><span class="sxs-lookup"><span data-stu-id="fec16-119">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a><span data-ttu-id="fec16-120">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="fec16-120">Possible Causes</span></span>

<span data-ttu-id="fec16-121">Se pasó un puntero NULL para un parámetro no opcional.</span><span class="sxs-lookup"><span data-stu-id="fec16-121">A NULL pointer was passed for a non-optional parameter.</span></span>

## <a name="fixes"></a><span data-ttu-id="fec16-122">Correcciones</span><span class="sxs-lookup"><span data-stu-id="fec16-122">Fixes</span></span>

<span data-ttu-id="fec16-123">Asegúrese de que un parámetro no opcional no tiene un puntero nulo.</span><span class="sxs-lookup"><span data-stu-id="fec16-123">Ensure that a non-optional parameter does not have a NULL pointer.</span></span>

 

 
