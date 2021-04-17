---
title: Network. receivedPackets
description: La propiedad receivedPackets recupera el número de paquetes recibidos.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Windows Media Player de red. receivedPackets
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc792330cd107ca428ad0fbec930fe262a2f131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700055"
---
# <a name="networkreceivedpackets"></a><span data-ttu-id="850fb-104">Network. receivedPackets</span><span class="sxs-lookup"><span data-stu-id="850fb-104">Network.receivedPackets</span></span>

<span data-ttu-id="850fb-105">La propiedad **receivedPackets** recupera el número de paquetes recibidos.</span><span class="sxs-lookup"><span data-stu-id="850fb-105">The **receivedPackets** property retrieves the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="850fb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="850fb-106">Syntax</span></span>

<span data-ttu-id="850fb-107">*reproductor*. *red*. **receivedPackets**</span><span class="sxs-lookup"><span data-stu-id="850fb-107">*player*.*network*.**receivedPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="850fb-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="850fb-108">Possible Values</span></span>

<span data-ttu-id="850fb-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="850fb-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="850fb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="850fb-110">Remarks</span></span>

<span data-ttu-id="850fb-111">Cada vez que se detiene y se reinicia la reproducción de un clip, esta propiedad se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="850fb-111">Each time clip playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="850fb-112">No se restablece si la reproducción de archivos está en pausa.</span><span class="sxs-lookup"><span data-stu-id="850fb-112">It is not reset if file playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="850fb-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="850fb-113">Examples</span></span>

<span data-ttu-id="850fb-114">En el siguiente ejemplo de JScript se usa *Network*. **receivedPackets** para mostrar el número de paquetes recibidos.</span><span class="sxs-lookup"><span data-stu-id="850fb-114">The following JScript example uses *Network*.**receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="850fb-115">La información se muestra en un DIV HTML creado con ID = "RP".</span><span class="sxs-lookup"><span data-stu-id="850fb-115">The information is displayed in an HTML DIV created with ID = "RP".</span></span> <span data-ttu-id="850fb-116">En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="850fb-116">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="850fb-117">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="850fb-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

```



## <a name="requirements"></a><span data-ttu-id="850fb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="850fb-118">Requirements</span></span>



| <span data-ttu-id="850fb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="850fb-119">Requirement</span></span> | <span data-ttu-id="850fb-120">Value</span><span class="sxs-lookup"><span data-stu-id="850fb-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="850fb-121">Versión</span><span class="sxs-lookup"><span data-stu-id="850fb-121">Version</span></span><br/> | <span data-ttu-id="850fb-122">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="850fb-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="850fb-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="850fb-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="850fb-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="850fb-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="850fb-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="850fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="850fb-126">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="850fb-126">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





