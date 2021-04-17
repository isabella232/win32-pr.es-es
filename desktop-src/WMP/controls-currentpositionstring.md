---
title: Controls. currentPositionString
description: La propiedad currentPositionString recupera la posición actual en el elemento multimedia como una cadena con el formato HH MM SS (horas, minutos y segundos).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Media Player de Windows Controls. currentPositionString
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700129"
---
# <a name="controlscurrentpositionstring"></a><span data-ttu-id="5def2-104">Controls. currentPositionString</span><span class="sxs-lookup"><span data-stu-id="5def2-104">Controls.currentPositionString</span></span>

<span data-ttu-id="5def2-105">La propiedad **currentPositionString** recupera la posición actual en el elemento multimedia como una **cadena** con el formato HH: mm: SS (horas, minutos y segundos).</span><span class="sxs-lookup"><span data-stu-id="5def2-105">The **currentPositionString** property retrieves the current position in the media item as a **String** formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a><span data-ttu-id="5def2-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5def2-106">Possible Values</span></span>

<span data-ttu-id="5def2-107">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5def2-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5def2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5def2-108">Remarks</span></span>

<span data-ttu-id="5def2-109">Si el elemento multimedia tiene menos de una hora, la parte HH: no se incluye.</span><span class="sxs-lookup"><span data-stu-id="5def2-109">If the media item is less than an hour long, the HH: portion is not included.</span></span>

> [!Note]  
> <span data-ttu-id="5def2-110">Debe incluir código para detener el temporizador cuando el elemento multimedia está detenido o en pausa.</span><span class="sxs-lookup"><span data-stu-id="5def2-110">You should include code to stop the timer when the media item is stopped or paused.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5def2-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5def2-111">Examples</span></span>

<span data-ttu-id="5def2-112">En el siguiente ejemplo de JScript se inicia un temporizador HTML que muestra la posición actual del archivo multimedia en intervalos de un segundo.</span><span class="sxs-lookup"><span data-stu-id="5def2-112">The following JScript example starts an HTML timer that displays the current position of the media file at one-second intervals.</span></span> <span data-ttu-id="5def2-113">Se creó un elemento de texto HTML denominado mi texto para mostrar la posición actual.</span><span class="sxs-lookup"><span data-stu-id="5def2-113">An HTML TEXT element named MyText was created to display the current position.</span></span> <span data-ttu-id="5def2-114">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5def2-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a><span data-ttu-id="5def2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5def2-115">Requirements</span></span>



| <span data-ttu-id="5def2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5def2-116">Requirement</span></span> | <span data-ttu-id="5def2-117">Value</span><span class="sxs-lookup"><span data-stu-id="5def2-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5def2-118">Versión</span><span class="sxs-lookup"><span data-stu-id="5def2-118">Version</span></span><br/> | <span data-ttu-id="5def2-119">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5def2-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5def2-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5def2-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="5def2-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5def2-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5def2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5def2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5def2-123">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="5def2-123">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





