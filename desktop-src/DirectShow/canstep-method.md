---
description: El método CanStep determina si el descodificador MPEG-2 del sistema local puede realizar la ejecución de fotogramas en una dirección especificada.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Método CanStep
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079921"
---
# <a name="canstep-method"></a><span data-ttu-id="a8c3e-103">Método CanStep</span><span class="sxs-lookup"><span data-stu-id="a8c3e-103">CanStep Method</span></span>

> [!Note]  
> <span data-ttu-id="a8c3e-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a8c3e-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a8c3e-106">El `CanStep` método determina si el descodificador MPEG-2 del sistema local puede realizar la ejecución paso a paso en una dirección especificada.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-106">The `CanStep` method determines whether the MPEG-2 decoder on the local system can perform frame stepping in a specified direction.</span></span>

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a><span data-ttu-id="a8c3e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8c3e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8c3e-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span><span class="sxs-lookup"><span data-stu-id="a8c3e-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span></span>
</dt> <dd>

<span data-ttu-id="a8c3e-109">Valor booleano que se usa como marcador para especificar la dirección, hacia delante o hacia atrás, de la capacidad de recorrido de fotogramas del descodificador.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-109">Boolean used as a flag to specify the direction, forward or backward, of decoder's frame-stepping ability.</span></span>



| <span data-ttu-id="a8c3e-110">Value</span><span class="sxs-lookup"><span data-stu-id="a8c3e-110">Value</span></span> | <span data-ttu-id="a8c3e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8c3e-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="a8c3e-112">true</span><span class="sxs-lookup"><span data-stu-id="a8c3e-112">true</span></span>  | <span data-ttu-id="a8c3e-113">¿Se puede descodificar el paso atrás?</span><span class="sxs-lookup"><span data-stu-id="a8c3e-113">Can decoder step backward?</span></span>                           |
| <span data-ttu-id="a8c3e-114">false</span><span class="sxs-lookup"><span data-stu-id="a8c3e-114">false</span></span> | <span data-ttu-id="a8c3e-115">¿El paso del descodificador puede avanzar?</span><span class="sxs-lookup"><span data-stu-id="a8c3e-115">Can decoder step forward?</span></span> <span data-ttu-id="a8c3e-116">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-116">This is the default value.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8c3e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8c3e-117">Return Value</span></span>

<span data-ttu-id="a8c3e-118">Devuelve un valor booleano true si el descodificador puede entrar en la dirección especificada y false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-118">Returns a Boolean value of true if the decoder can step in the specified direction, and false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8c3e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8c3e-119">Remarks</span></span>

<span data-ttu-id="a8c3e-120">No todos los descodificadores MPEG-2 de hardware admiten las nuevas capacidades de recorrido de fotogramas en DirectShow® 8,0.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-120">Not all hardware MPEG-2 decoders support the new frame stepping capabilities in DirectShow® 8.0.</span></span> <span data-ttu-id="a8c3e-121">Este método consulta el descodificador para obtener la funcionalidad de ejecución de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-121">This method queries the decoder for its frame stepping capabilities.</span></span> <span data-ttu-id="a8c3e-122">Si el descodificador puede realizar la ejecución paso a paso, una aplicación puede utilizar el método [**Step**](step-method.md) para recorrer los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-122">If the decoder can perform frame stepping, an application can use the [**Step**](step-method.md) method to step through frames.</span></span> <span data-ttu-id="a8c3e-123">Este método siempre devolverá **true** si se usa un descodificador de software.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-123">This method will always return **true** if a software decoder is being used.</span></span>

 

 



