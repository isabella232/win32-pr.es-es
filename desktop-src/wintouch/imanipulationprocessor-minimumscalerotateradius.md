---
title: Propiedad MinimumScaleRotateRadius de IManipulationProcessor
description: Especifica el tamaño de los contactos de distancia de un gesto de escala o giro que debe ser el desencadenador de la manipulación.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- Propiedad MinimumScaleRotateRadius Touch de Windows
- Propiedad MinimumScaleRotateRadius Touch de Windows, interfaz IManipulationProcessor
- Interfaz IManipulationProcessor Touch de Windows, propiedad MinimumScaleRotateRadius
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784156"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a><span data-ttu-id="3602e-106">IManipulationProcessor:: MinimumScaleRotateRadius (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3602e-106">IManipulationProcessor::MinimumScaleRotateRadius property</span></span>

<span data-ttu-id="3602e-107">Especifica el tamaño de los contactos de distancia de un gesto de escala o giro que debe ser el desencadenador de la manipulación.</span><span class="sxs-lookup"><span data-stu-id="3602e-107">Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation.</span></span>

<span data-ttu-id="3602e-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3602e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3602e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3602e-109">Syntax</span></span>


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a><span data-ttu-id="3602e-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3602e-110">Property value</span></span>

<span data-ttu-id="3602e-111">Especifica la distancia mínima entre contactos para desencadenar gestos de escala o giro.</span><span class="sxs-lookup"><span data-stu-id="3602e-111">Specifies the minimum distance between contacts to trigger scale or rotate gestures.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3602e-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3602e-112">Error codes</span></span>

## <a name="remarks"></a><span data-ttu-id="3602e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3602e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3602e-114">Esta propiedad se establece en centipixels (100 $ de un píxel).</span><span class="sxs-lookup"><span data-stu-id="3602e-114">This property is set in centipixels (100ths of a pixel).</span></span>

 

<span data-ttu-id="3602e-115">Si se establece este valor, el procesador de manipulación pasará por alto los gestos que tengan un radio demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="3602e-115">Setting this value will make the manipulation processor ignore gestures that have too small of a radius.</span></span> <span data-ttu-id="3602e-116">Esto resulta útil si desea evitar que un usuario manipule un objeto en un valor demasiado pequeño de un radio.</span><span class="sxs-lookup"><span data-stu-id="3602e-116">This is useful if you want to prevent a user from manipulating an object to too small of a radius.</span></span> <span data-ttu-id="3602e-117">Por ejemplo, si usa un procesador de manipulación con un círculo y desea asegurarse de que mantiene un radio superior a 100 píxeles, debe establecer este valor en 10000.</span><span class="sxs-lookup"><span data-stu-id="3602e-117">For example, if you are using a manipulation processor with a circle and want the ensure that it maintains a radius greater than 100 pixels, you would set this value to 10000.</span></span>

## <a name="examples"></a><span data-ttu-id="3602e-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3602e-118">Examples</span></span>


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a><span data-ttu-id="3602e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="3602e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3602e-120">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="3602e-120">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




