---
description: La propiedad PlayState recupera el estado actual del objeto MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Propiedad PlayState
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686338"
---
# <a name="playstate-property"></a><span data-ttu-id="c1d1c-103">Propiedad PlayState</span><span class="sxs-lookup"><span data-stu-id="c1d1c-103">PlayState Property</span></span>

> [!Note]  
> <span data-ttu-id="c1d1c-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c1d1c-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c1d1c-106">La `PlayState` propiedad recupera el estado actual del objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="c1d1c-106">The `PlayState` property retrieves the current state of the **MSWebDVD** object.</span></span>

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a><span data-ttu-id="c1d1c-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1d1c-107">Return Value</span></span>

<span data-ttu-id="c1d1c-108">Devuelve un valor entero que representa el estado actual del navegador del DVD.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-108">Returns an Integer value representing the current state of the DVD Navigator.</span></span>



| <span data-ttu-id="c1d1c-109">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c1d1c-109">Return code</span></span> | <span data-ttu-id="c1d1c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1d1c-110">Description</span></span>   |
|-------------|---------------|
| <span data-ttu-id="c1d1c-111">-2</span><span class="sxs-lookup"><span data-stu-id="c1d1c-111">-2</span></span>          | <span data-ttu-id="c1d1c-112">No definido</span><span class="sxs-lookup"><span data-stu-id="c1d1c-112">Undefined</span></span>     |
| <span data-ttu-id="c1d1c-113">-1</span><span class="sxs-lookup"><span data-stu-id="c1d1c-113">-1</span></span>          | <span data-ttu-id="c1d1c-114">No inicializado</span><span class="sxs-lookup"><span data-stu-id="c1d1c-114">Uninitialized</span></span> |
| <span data-ttu-id="c1d1c-115">0</span><span class="sxs-lookup"><span data-stu-id="c1d1c-115">0</span></span>           | <span data-ttu-id="c1d1c-116">Detenido</span><span class="sxs-lookup"><span data-stu-id="c1d1c-116">Stopped</span></span>       |
| <span data-ttu-id="c1d1c-117">1</span><span class="sxs-lookup"><span data-stu-id="c1d1c-117">1</span></span>           | <span data-ttu-id="c1d1c-118">En pausa</span><span class="sxs-lookup"><span data-stu-id="c1d1c-118">Paused</span></span>        |
| <span data-ttu-id="c1d1c-119">2</span><span class="sxs-lookup"><span data-stu-id="c1d1c-119">2</span></span>           | <span data-ttu-id="c1d1c-120">En ejecución</span><span class="sxs-lookup"><span data-stu-id="c1d1c-120">Running</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="c1d1c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1d1c-121">Remarks</span></span>

<span data-ttu-id="c1d1c-122">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="c1d1c-123">El objeto **MSWebDVD** controla el filtro de navegador de DVD de DirectShow, que realiza el trabajo real de la navegación por DVD.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-123">The **MSWebDVD** object controls the DirectShow DVD Navigator filter, which does the actual work of DVD navigation.</span></span> <span data-ttu-id="c1d1c-124">En realidad, es el estado del navegador de DVD al que hace referencia esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-124">It is actually the state of the DVD Navigator that this property refers to.</span></span> <span data-ttu-id="c1d1c-125">El navegador de DVD puede estar en uno de varios Estados, tal y como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-125">The DVD Navigator can be in one of several states, as described above.</span></span> <span data-ttu-id="c1d1c-126">La `PlayState` propiedad puede ser útil como herramienta de diagnóstico, pero generalmente no debería haber ninguna razón para que una aplicación de scripts supervise el estado del navegador del DVD.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-126">The `PlayState` property can be useful as a diagnostic tool, but generally there should be no reason for a scripting application to monitor the state of the DVD Navigator.</span></span>

 

 



