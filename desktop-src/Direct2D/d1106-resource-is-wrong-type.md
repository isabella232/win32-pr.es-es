---
title: El recurso D1106 es de tipo incorrecto
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: El recurso especificado no es del tipo esperado.
keywords:
- El recurso D1106 es de tipo incorrecto Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105650231"
---
# <a name="d1106-resource-is-wrong-type"></a><span data-ttu-id="1496e-104">D1106: el tipo de recurso es incorrecto</span><span class="sxs-lookup"><span data-stu-id="1496e-104">D1106: Resource Is Wrong Type</span></span>

<span data-ttu-id="1496e-105">El \[ *recurso* \] de recurso especificado no es del tipo esperado.</span><span class="sxs-lookup"><span data-stu-id="1496e-105">The given resource \[*resource*\] is not of an expected type.</span></span>

## <a name="placeholders"></a><span data-ttu-id="1496e-106">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="1496e-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="1496e-107"><span id="resource"></span><span id="RESOURCE"></span>*recurso*</span><span class="sxs-lookup"><span data-stu-id="1496e-107"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="1496e-108">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="1496e-108">The address of the resource.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="1496e-109">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="1496e-109">Possible Causes</span></span>

<span data-ttu-id="1496e-110">Una interfaz se convierta incorrectamente y se usó como parámetro para un método o una función.</span><span class="sxs-lookup"><span data-stu-id="1496e-110">An interface was improperly cast and used as a parameter for a method or function.</span></span>

## <a name="examples"></a><span data-ttu-id="1496e-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1496e-111">Examples</span></span>

<span data-ttu-id="1496e-112">En el ejemplo siguiente se pasa un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) cuando se espera un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .</span><span class="sxs-lookup"><span data-stu-id="1496e-112">The following example passes an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) when an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) is expected.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



<span data-ttu-id="1496e-113">Este ejemplo genera el siguiente mensaje de depuración:</span><span class="sxs-lookup"><span data-stu-id="1496e-113">This example produces the following debug message:</span></span>

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a><span data-ttu-id="1496e-114">Correcciones</span><span class="sxs-lookup"><span data-stu-id="1496e-114">Fixes</span></span>

<span data-ttu-id="1496e-115">Use el tipo requerido por el método.</span><span class="sxs-lookup"><span data-stu-id="1496e-115">Use the type required by the method.</span></span>

 

 
