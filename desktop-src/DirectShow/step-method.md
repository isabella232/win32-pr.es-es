---
description: El método Step avanza el flujo de DVD-Video por el número especificado de fotogramas.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Método Step
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678262"
---
# <a name="step-method"></a><span data-ttu-id="51587-103">Método Step</span><span class="sxs-lookup"><span data-stu-id="51587-103">Step Method</span></span>

> [!Note]  
> <span data-ttu-id="51587-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="51587-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="51587-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="51587-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="51587-106">El `Step` método avanza el flujo de DVD-Video por el número de fotogramas especificado.</span><span class="sxs-lookup"><span data-stu-id="51587-106">The `Step` method advances the DVD-Video stream by the specified number of frames.</span></span>

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a><span data-ttu-id="51587-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51587-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51587-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span><span class="sxs-lookup"><span data-stu-id="51587-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="51587-109">Especifica el número de fotogramas que se van a recorrer como un entero.</span><span class="sxs-lookup"><span data-stu-id="51587-109">Specifies the number of frames to step as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51587-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51587-110">Return Value</span></span>

<span data-ttu-id="51587-111">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="51587-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51587-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51587-112">Remarks</span></span>

<span data-ttu-id="51587-113">Antes de llamar a este método, llame a [**CanStep**](canstep-method.md) para determinar si el descodificador admite la ejecución de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="51587-113">Before calling this method, call [**CanStep**](canstep-method.md) to determine whether the decoder supports frame stepping.</span></span>

<span data-ttu-id="51587-114">Si el DVD-Video se está reproduciendo en modo inverso cuando se llama a este método y el descodificador admite el recorrido de fotogramas inverso, el fotograma se ejecuta en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="51587-114">If the DVD-Video is playing in reverse mode when this method is called, and the decoder supports reverse frame stepping, then the frame stepping is done in reverse.</span></span>

 

 



