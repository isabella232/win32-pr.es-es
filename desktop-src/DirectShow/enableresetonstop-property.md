---
description: La propiedad EnableResetOnStop establece o recupera un valor que determina cómo se reanudará la reproducción cuando el gráfico de filtros realice una transición desde un estado detenido.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Propiedad EnableResetOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806134"
---
# <a name="enableresetonstop-property"></a><span data-ttu-id="f6035-103">Propiedad EnableResetOnStop</span><span class="sxs-lookup"><span data-stu-id="f6035-103">EnableResetOnStop Property</span></span>

> [!Note]  
> <span data-ttu-id="f6035-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f6035-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f6035-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="f6035-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f6035-106">La `EnableResetOnStop` propiedad establece o recupera un valor que determina cómo se reanudará la reproducción cuando el gráfico de filtros realice una transición desde un estado detenido.</span><span class="sxs-lookup"><span data-stu-id="f6035-106">The `EnableResetOnStop` property sets or retrieves a value that determines how play will resume when the filter graph makes a transition from a stopped state.</span></span>

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a><span data-ttu-id="f6035-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6035-107">Return Value</span></span>

<span data-ttu-id="f6035-108">Devuelve un valor booleano que indica dónde se iniciará la reproducción del objeto MSWebDVD de nuevo después de que se detenga el gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="f6035-108">Returns a Boolean value indicating where the MSWebDVD object will start playing again after the filter graph is stopped.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6035-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6035-109">Remarks</span></span>

<span data-ttu-id="f6035-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f6035-110">This property is read/write.</span></span>

<span data-ttu-id="f6035-111">Los valores posibles de esta propiedad son: con el valor predeterminado True.</span><span class="sxs-lookup"><span data-stu-id="f6035-111">The possible values of this property are: with a default value of true.</span></span>



| <span data-ttu-id="f6035-112">Value</span><span class="sxs-lookup"><span data-stu-id="f6035-112">Value</span></span> | <span data-ttu-id="f6035-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6035-113">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6035-114">true</span><span class="sxs-lookup"><span data-stu-id="f6035-114">true</span></span>  | <span data-ttu-id="f6035-115">El navegador de DVD se restablecerá y comenzará a reproducir desde el principio del disco. Este es el valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f6035-115">DVD Navigator will reset and start play from the beginning of the disc. This is the default value</span></span> |
| <span data-ttu-id="f6035-116">false</span><span class="sxs-lookup"><span data-stu-id="f6035-116">false</span></span> | <span data-ttu-id="f6035-117">El navegador de DVD se reanudará en el punto en que se quedó.</span><span class="sxs-lookup"><span data-stu-id="f6035-117">DVD Navigator will resume play where it left off.</span></span>                                                 |



 

 

 



