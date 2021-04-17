---
description: El método Render inicializa el gráfico de filtros de DVD.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Método Render
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677091"
---
# <a name="render-method"></a><span data-ttu-id="c0c0b-103">Método Render</span><span class="sxs-lookup"><span data-stu-id="c0c0b-103">Render Method</span></span>

> [!Note]  
> <span data-ttu-id="c0c0b-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c0c0b-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c0c0b-106">El `Render` método inicializa el gráfico de filtros de DVD.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-106">The `Render` method initializes the DVD filter graph.</span></span>

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a><span data-ttu-id="c0c0b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0c0b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0c0b-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span><span class="sxs-lookup"><span data-stu-id="c0c0b-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span></span>
</dt> <dd>

<span data-ttu-id="c0c0b-109">Especifica un valor entero que indica si el gráfico de filtro se destruirá y se volverá a generar.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-109">Specifies an integer value indicating whether the filter graph will be destroyed and rebuilt.</span></span>



| <span data-ttu-id="c0c0b-110">Value</span><span class="sxs-lookup"><span data-stu-id="c0c0b-110">Value</span></span> | <span data-ttu-id="c0c0b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0c0b-111">Description</span></span>                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c0b-112">0</span><span class="sxs-lookup"><span data-stu-id="c0c0b-112">0</span></span>     | <span data-ttu-id="c0c0b-113">El gráfico de filtro no se destruirá y se volverá a generar si ya existe.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-113">The filter graph will not be destroyed and rebuilt if it already exists.</span></span> <span data-ttu-id="c0c0b-114">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-114">This is the default value.</span></span> |
| <span data-ttu-id="c0c0b-115">1</span><span class="sxs-lookup"><span data-stu-id="c0c0b-115">1</span></span>     | <span data-ttu-id="c0c0b-116">El gráfico de filtro se destruirá y se volverá a generar si ya existe.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-116">The filter graph will be destroyed and rebuilt if it already exists.</span></span>                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0c0b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0c0b-117">Return Value</span></span>

<span data-ttu-id="c0c0b-118">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0c0b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0c0b-119">Remarks</span></span>

<span data-ttu-id="c0c0b-120">El `Render` método permite al objeto **MSWebDVD** inicializar por completo el gráfico de filtros de DirectShow subyacente en el inicio.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-120">The `Render` method enables the **MSWebDVD** object to fully initialize the underlying DirectShow filter graph on startup.</span></span> <span data-ttu-id="c0c0b-121">Esto elimina el leve retraso que, de lo contrario, se produce cuando el usuario emite el primer comando para reproducir un disco o para mostrar un menú.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-121">This eliminates the slight delay that otherwise occurs when the user issues the first command to play a disc or show a menu.</span></span> <span data-ttu-id="c0c0b-122">No hay ningún caso en el que `Render` sea necesario llamar antes de llamar a cualquier otro método.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-122">There is no case in which `Render` needs to be called before calling any other method.</span></span> <span data-ttu-id="c0c0b-123">Por ejemplo, si la aplicación llama a [**PlayTitle**](playtitle-method.md) antes de que se haya inicializado el gráfico de filtros, el objeto **MSWebDVD** llama `Render` automáticamente a antes de intentar reproducir el disco.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-123">For example, if the application calls [**PlayTitle**](playtitle-method.md) before the filter graph has been initialized, the **MSWebDVD** object calls `Render` automatically before attempting to play the disc.</span></span>

 

 



