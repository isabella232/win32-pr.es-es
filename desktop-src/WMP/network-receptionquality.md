---
title: Network. receptionQuality
description: La propiedad receptionQuality recupera el porcentaje de paquetes recibidos en los últimos 30 segundos.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Windows Media Player de red. receptionQuality
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706ba4d953f80c4a9e799971a7e73d49553c709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700054"
---
# <a name="networkreceptionquality"></a><span data-ttu-id="f0d2d-104">Network. receptionQuality</span><span class="sxs-lookup"><span data-stu-id="f0d2d-104">Network.receptionQuality</span></span>

<span data-ttu-id="f0d2d-105">La propiedad **receptionQuality** recupera el porcentaje de paquetes recibidos en los últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="f0d2d-105">The **receptionQuality** property retrieves the percentage of packets received in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d2d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0d2d-106">Syntax</span></span>

<span data-ttu-id="f0d2d-107">*reproductor*. *red*. **receptionQuality**</span><span class="sxs-lookup"><span data-stu-id="f0d2d-107">*player*.*network*.**receptionQuality**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f0d2d-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f0d2d-108">Possible Values</span></span>

<span data-ttu-id="f0d2d-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="f0d2d-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f0d2d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0d2d-110">Remarks</span></span>

<span data-ttu-id="f0d2d-111">El número de paquetes recibidos, perdidos y recuperados durante el streaming se supervisa una vez por segundo.</span><span class="sxs-lookup"><span data-stu-id="f0d2d-111">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="f0d2d-112">**receptionQuality** es el porcentaje de paquetes que no se pierden durante los últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="f0d2d-112">**receptionQuality** is the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="f0d2d-113">Cada vez que se detiene y se reinicia la reproducción, esta propiedad se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="f0d2d-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="f0d2d-114">No se restablece si la reproducción está en pausa.</span><span class="sxs-lookup"><span data-stu-id="f0d2d-114">It is not reset if playback is paused.</span></span>

<span data-ttu-id="f0d2d-115">Esta propiedad devuelve información válida solo durante el tiempo de ejecución y solo si el *reproductor*. También se establece la propiedad **URL** .</span><span class="sxs-lookup"><span data-stu-id="f0d2d-115">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span>

## <a name="examples"></a><span data-ttu-id="f0d2d-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f0d2d-116">Examples</span></span>

<span data-ttu-id="f0d2d-117">En el siguiente ejemplo de JScript se usa *Network*. **receptionQuality** para mostrar el porcentaje de paquetes recibidos.</span><span class="sxs-lookup"><span data-stu-id="f0d2d-117">The following JScript example uses *Network*.**receptionQuality** to display the percentage of packets received.</span></span> <span data-ttu-id="f0d2d-118">La información se muestra en un DIV HTML creado con ID = "PET".</span><span class="sxs-lookup"><span data-stu-id="f0d2d-118">The information is displayed in an HTML DIV created with ID = "RQ".</span></span> <span data-ttu-id="f0d2d-119">En el ejemplo se usa un temporizador con un intervalo de 30 segundos para actualizar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f0d2d-119">The example uses a timer with a 30-second interval to update the display.</span></span> <span data-ttu-id="f0d2d-120">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f0d2d-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="f0d2d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0d2d-121">Requirements</span></span>



| <span data-ttu-id="f0d2d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0d2d-122">Requirement</span></span> | <span data-ttu-id="f0d2d-123">Value</span><span class="sxs-lookup"><span data-stu-id="f0d2d-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d2d-124">Versión</span><span class="sxs-lookup"><span data-stu-id="f0d2d-124">Version</span></span><br/> | <span data-ttu-id="f0d2d-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f0d2d-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f0d2d-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0d2d-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f0d2d-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0d2d-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0d2d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0d2d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d2d-129">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="f0d2d-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="f0d2d-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="f0d2d-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





