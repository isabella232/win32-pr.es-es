---
title: Network. downloadProgress
description: La propiedad downloadProgress recupera el porcentaje de descarga completada.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Windows Media Player de red. downloadProgress
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605d7d08b346c5cc279176098b2a6d593a2fb925
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708305"
---
# <a name="networkdownloadprogress"></a><span data-ttu-id="2a2e8-104">Network. downloadProgress</span><span class="sxs-lookup"><span data-stu-id="2a2e8-104">Network.downloadProgress</span></span>

<span data-ttu-id="2a2e8-105">La propiedad **downloadProgress** recupera el porcentaje de descarga completada.</span><span class="sxs-lookup"><span data-stu-id="2a2e8-105">The **downloadProgress** property retrieves the percentage of download completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a2e8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a2e8-106">Syntax</span></span>

<span data-ttu-id="2a2e8-107">*reproductor*. *red*. **downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="2a2e8-107">*player*.*network*.**downloadProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="2a2e8-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="2a2e8-108">Possible Values</span></span>

<span data-ttu-id="2a2e8-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="2a2e8-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2a2e8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a2e8-110">Remarks</span></span>

<span data-ttu-id="2a2e8-111">Cuando el control de Media Player de Windows se conecta a un archivo multimedia que se puede reproducir y descargar al mismo tiempo, la propiedad **downloadProgress** devuelve el porcentaje del archivo total que se ha descargado.</span><span class="sxs-lookup"><span data-stu-id="2a2e8-111">When the Windows Media Player control is connected to a media file that can be played and downloaded at the same time, the **downloadProgress** property returns the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="2a2e8-112">Actualmente, esta característica solo se admite en servidores Web.</span><span class="sxs-lookup"><span data-stu-id="2a2e8-112">This feature is currently supported only on web servers.</span></span> <span data-ttu-id="2a2e8-113">Los siguientes formatos de archivo se pueden descargar y reproducir simultáneamente:</span><span class="sxs-lookup"><span data-stu-id="2a2e8-113">The following file formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="2a2e8-114">Formato ASF</span><span class="sxs-lookup"><span data-stu-id="2a2e8-114">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="2a2e8-115">Audio de Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="2a2e8-115">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="2a2e8-116">Vídeo de Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="2a2e8-116">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="2a2e8-117">MP3</span><span class="sxs-lookup"><span data-stu-id="2a2e8-117">MP3</span></span>
-   <span data-ttu-id="2a2e8-118">MPEG</span><span class="sxs-lookup"><span data-stu-id="2a2e8-118">MPEG</span></span>
-   <span data-ttu-id="2a2e8-119">WAV</span><span class="sxs-lookup"><span data-stu-id="2a2e8-119">WAV</span></span>
-   <span data-ttu-id="2a2e8-120">Algunos archivos AVI</span><span class="sxs-lookup"><span data-stu-id="2a2e8-120">Some AVI files</span></span>

<span data-ttu-id="2a2e8-121">Use el *reproductor*. Evento de **almacenamiento en búfer** para determinar cuándo comienza y termina la descarga.</span><span class="sxs-lookup"><span data-stu-id="2a2e8-121">Use the *Player*.**Buffering** event to determine when the downloading begins and ends.</span></span>

## <a name="examples"></a><span data-ttu-id="2a2e8-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2a2e8-122">Examples</span></span>

<span data-ttu-id="2a2e8-123">En el siguiente ejemplo de JScript se usa *Network*. **downloadProgress** para mostrar el porcentaje de descarga completada.</span><span class="sxs-lookup"><span data-stu-id="2a2e8-123">The following JScript example uses *Network*.**downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="2a2e8-124">La información se muestra en un DIV HTML creado con ID = "DP".</span><span class="sxs-lookup"><span data-stu-id="2a2e8-124">The information is displayed in an HTML DIV created with ID = "DP".</span></span> <span data-ttu-id="2a2e8-125">En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2a2e8-125">The example uses a timer with a 1 second interval to update the display.</span></span> <span data-ttu-id="2a2e8-126">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2a2e8-126">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="2a2e8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a2e8-127">Requirements</span></span>



| <span data-ttu-id="2a2e8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a2e8-128">Requirement</span></span> | <span data-ttu-id="2a2e8-129">Value</span><span class="sxs-lookup"><span data-stu-id="2a2e8-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a2e8-130">Versión</span><span class="sxs-lookup"><span data-stu-id="2a2e8-130">Version</span></span><br/> | <span data-ttu-id="2a2e8-131">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2a2e8-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2a2e8-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2a2e8-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="2a2e8-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a2e8-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a2e8-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a2e8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a2e8-135">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="2a2e8-135">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="2a2e8-136">**Evento Player. buffering**</span><span class="sxs-lookup"><span data-stu-id="2a2e8-136">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> </dl>

 

 





