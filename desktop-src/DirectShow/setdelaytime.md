---
description: El método SetDelayTime establece el tiempo de retraso para la información sobre herramientas asociada al objeto MSWebDVD.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494194"
---
# <a name="setdelaytime"></a><span data-ttu-id="f2e62-103">SetDelayTime</span><span class="sxs-lookup"><span data-stu-id="f2e62-103">SetDelayTime</span></span>

> [!Note]  
> <span data-ttu-id="f2e62-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f2e62-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f2e62-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="f2e62-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f2e62-106">El `SetDelayTime` método establece el tiempo de retraso para la información sobre herramientas asociada al objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="f2e62-106">The `SetDelayTime` method sets the delay time for the ToolTip associated with the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a><span data-ttu-id="f2e62-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2e62-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e62-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span><span class="sxs-lookup"><span data-stu-id="f2e62-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span></span>
</dt> <dd>

<span data-ttu-id="f2e62-109">Especifica el tipo de retraso como un entero.</span><span class="sxs-lookup"><span data-stu-id="f2e62-109">Specifies the type of delay as an Integer.</span></span>



| <span data-ttu-id="f2e62-110">Value</span><span class="sxs-lookup"><span data-stu-id="f2e62-110">Value</span></span> | <span data-ttu-id="f2e62-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2e62-111">Description</span></span>                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e62-112">-1</span><span class="sxs-lookup"><span data-stu-id="f2e62-112">-1</span></span>    | <span data-ttu-id="f2e62-113">Para restablecer el tiempo de retraso de autopop en su valor predeterminado, establezca *iNewVal* en-1.</span><span class="sxs-lookup"><span data-stu-id="f2e62-113">To reset the autopop delay time to its default value, set *iNewVal* to -1.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="f2e62-114">0</span><span class="sxs-lookup"><span data-stu-id="f2e62-114">0</span></span>     | <span data-ttu-id="f2e62-115">Establece el tiempo durante el que una ventana de información sobre herramientas permanece visible si el puntero es estacionario dentro del rectángulo delimitador de una herramienta.</span><span class="sxs-lookup"><span data-stu-id="f2e62-115">Set the length of time a ToolTip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span>                                                                                                                         |
| <span data-ttu-id="f2e62-116">1</span><span class="sxs-lookup"><span data-stu-id="f2e62-116">1</span></span>     | <span data-ttu-id="f2e62-117">Establezca el período de tiempo que un puntero debe permanecer estacionario dentro del rectángulo delimitador de una herramienta antes de que aparezca la ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="f2e62-117">Set the length of time a pointer must remain stationary within a tool's bounding rectangle before the ToolTip window appears.</span></span>                                                                                                                    |
| <span data-ttu-id="f2e62-118">2</span><span class="sxs-lookup"><span data-stu-id="f2e62-118">2</span></span>     | <span data-ttu-id="f2e62-119">Establezca la cantidad de tiempo que tardará en aparecer la siguiente ventana de información sobre herramientas cuando el puntero se mueva de una herramienta a otra.</span><span class="sxs-lookup"><span data-stu-id="f2e62-119">Set the length of time it takes for subsequent ToolTip windows to appear as the pointer moves from one tool to another.</span></span>                                                                                                                          |
| <span data-ttu-id="f2e62-120">3</span><span class="sxs-lookup"><span data-stu-id="f2e62-120">3</span></span>     | <span data-ttu-id="f2e62-121">Establecer todos los tiempos de retraso en las proporciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="f2e62-121">Set all delay times to default proportions.</span></span> <span data-ttu-id="f2e62-122">La hora de autopop es diez veces la hora inicial y la hora de la representación es una quinta la hora inicial.</span><span class="sxs-lookup"><span data-stu-id="f2e62-122">The autopop time is ten times the initial time and the reshow time is one-fifth the initial time.</span></span> <span data-ttu-id="f2e62-123">Si se establece esta marca, use un valor positivo de iNewVal para especificar el tiempo inicial, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="f2e62-123">If this flag is set, use a positive value of iNewVal to specify the initial time, in milliseconds.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f2e62-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span><span class="sxs-lookup"><span data-stu-id="f2e62-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span></span>
</dt> <dd>

<span data-ttu-id="f2e62-125">Especifica el retraso, en milisegundos, como un entero.</span><span class="sxs-lookup"><span data-stu-id="f2e62-125">Specifies the delay, in milliseconds, as an Integer.</span></span>



| <span data-ttu-id="f2e62-126">Value</span><span class="sxs-lookup"><span data-stu-id="f2e62-126">Value</span></span>                    | <span data-ttu-id="f2e62-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2e62-127">Description</span></span>                                                   |
|--------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f2e62-128">-1</span><span class="sxs-lookup"><span data-stu-id="f2e62-128">-1</span></span>                       | <span data-ttu-id="f2e62-129">Establece el retraso especificado en *iDelayType* en su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f2e62-129">Sets the delay specified in *iDelayType* to its default value</span></span> |
| <span data-ttu-id="f2e62-130">cualquier otro valor negativo</span><span class="sxs-lookup"><span data-stu-id="f2e62-130">any other negative value</span></span> | <span data-ttu-id="f2e62-131">Establece todos los tipos de retraso en su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f2e62-131">Sets all delay types to their default value.</span></span>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e62-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2e62-132">Return Value</span></span>

<span data-ttu-id="f2e62-133">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f2e62-133">No return value.</span></span>

 

 



