---
title: Network.downloadProgress
description: La propiedad downloadProgress recupera el porcentaje de descarga completada.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Network.downloadProgress Reproductor de Windows Media
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
ms.openlocfilehash: ffc8d2707cd5fc24129363d53f9ee58fedf7b15c5da4eb5b80f032524ee66c09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901725"
---
# <a name="networkdownloadprogress"></a>Network.downloadProgress

La **propiedad downloadProgress** recupera el porcentaje de descarga completada.

## <a name="syntax"></a>Syntax

*player*. *network*. **downloadProgress**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Cuando el control Reproductor de Windows Media está conectado a un archivo multimedia que se puede reproducir y descargar al mismo tiempo, la propiedad **downloadProgress** devuelve el porcentaje del archivo total que se ha descargado. Actualmente, esta característica solo se admite en servidores web. Los siguientes formatos de archivo se pueden descargar y reproducir simultáneamente:

-   Formato ASF
-   Audio de Windows Media (WMA)
-   Vídeo de Windows Media (WMV)
-   MP3
-   MPEG
-   WAV
-   Algunos archivos AVI

Use el *reproductor*. **Evento de** almacenamiento en búfer para determinar cuándo comienza y finaliza la descarga.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **downloadProgress para** mostrar el porcentaje de descarga completada. La información se muestra en una DIV HTML creada con id. = "DP". En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla. El **objeto Player** se creó con id. = "Player".


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player.Buffering (Evento)**](player-player-buffering.md)
</dt> </dl>

 

 





