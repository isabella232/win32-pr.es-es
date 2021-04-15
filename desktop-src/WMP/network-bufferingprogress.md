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
# <a name="networkbufferingprogress"></a>Network. bufferingProgress

La propiedad **bufferingProgress** recupera el porcentaje de almacenamiento en búfer completado.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **bufferingProgress**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="remarks"></a>Observaciones

Cada vez que se detiene y se reinicia la reproducción, esta propiedad se establece en cero. No se restablece si la reproducción está en pausa.

El almacenamiento en búfer solo se aplica al contenido de streaming. Esta propiedad devuelve información válida solo durante el tiempo de ejecución, cuando el *reproductor*. La propiedad de **dirección URL** está establecida.

Use el evento *Player*. * * * * buffering * * * * para determinar cuándo se inicia o se detiene el almacenamiento en búfer.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **bufferingProgress** para mostrar el porcentaje de almacenamiento en búfer completado. La información se muestra en un DIV HTML creado con ID = "BP". En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla. El objeto **Player** se creó con ID = "Player".


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Evento Player. buffering**](player-player-buffering.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





