---
title: Network. bufferingProgress
description: La propiedad bufferingProgress recupera el porcentaje de almacenamiento en búfer completado.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Windows Media Player de red. bufferingProgress
topic_type:
- apiref
api_name:
- Network.bufferingProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e3a4f37f8f6b8ffe8ff93ca72b0c9551d7e314
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708308"
---
# <a name="networkbufferingprogress"></a><span data-ttu-id="a724c-104">Network. bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="a724c-104">Network.bufferingProgress</span></span>

<span data-ttu-id="a724c-105">La propiedad **bufferingProgress** recupera el porcentaje de almacenamiento en búfer completado.</span><span class="sxs-lookup"><span data-stu-id="a724c-105">The **bufferingProgress** property retrieves the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a724c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a724c-106">Syntax</span></span>

<span data-ttu-id="a724c-107">*reproductor*. *red*. **bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="a724c-107">*player*.*network*.**bufferingProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a724c-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a724c-108">Possible Values</span></span>

<span data-ttu-id="a724c-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="a724c-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="a724c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a724c-110">Remarks</span></span>

<span data-ttu-id="a724c-111">Cada vez que se detiene y se reinicia la reproducción, esta propiedad se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="a724c-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="a724c-112">No se restablece si la reproducción está en pausa.</span><span class="sxs-lookup"><span data-stu-id="a724c-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="a724c-113">El almacenamiento en búfer solo se aplica al contenido de streaming.</span><span class="sxs-lookup"><span data-stu-id="a724c-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="a724c-114">Esta propiedad devuelve información válida solo durante el tiempo de ejecución, cuando el *reproductor*. La propiedad de **dirección URL** está establecida.</span><span class="sxs-lookup"><span data-stu-id="a724c-114">This property returns valid information only during run time, when the *Player*.**URL** property is set.</span></span>

<span data-ttu-id="a724c-115">Use el evento *Player*. \* \* \* \* buffering \* \* \* \* para determinar cuándo se inicia o se detiene el almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="a724c-115">Use the *Player*.\*\*\*\*Buffering\*\*\*\* event to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="a724c-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a724c-116">Examples</span></span>

<span data-ttu-id="a724c-117">En el siguiente ejemplo de JScript se usa *Network*. **bufferingProgress** para mostrar el porcentaje de almacenamiento en búfer completado.</span><span class="sxs-lookup"><span data-stu-id="a724c-117">The following JScript example uses *Network*.**bufferingProgress** to display the percentage of buffering completed.</span></span> <span data-ttu-id="a724c-118">La información se muestra en un DIV HTML creado con ID = "BP".</span><span class="sxs-lookup"><span data-stu-id="a724c-118">The information is displayed in an HTML DIV created with ID = "BP".</span></span> <span data-ttu-id="a724c-119">En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a724c-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="a724c-120">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a724c-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.

   // Test whether buffering has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdateBP()", 1000);
   }

   else{
      // Buffering is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateBP(){
   BP.innerHTML = "";
   BP.innerHTML = "Buffering progress: " + Player.network.bufferingProgress;
   BP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="a724c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a724c-121">Requirements</span></span>



| <span data-ttu-id="a724c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a724c-122">Requirement</span></span> | <span data-ttu-id="a724c-123">Value</span><span class="sxs-lookup"><span data-stu-id="a724c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a724c-124">Versión</span><span class="sxs-lookup"><span data-stu-id="a724c-124">Version</span></span><br/> | <span data-ttu-id="a724c-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a724c-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a724c-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a724c-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="a724c-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a724c-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a724c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a724c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a724c-129">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="a724c-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="a724c-130">**Evento Player. buffering**</span><span class="sxs-lookup"><span data-stu-id="a724c-130">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> <dt>

[<span data-ttu-id="a724c-131">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="a724c-131">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





