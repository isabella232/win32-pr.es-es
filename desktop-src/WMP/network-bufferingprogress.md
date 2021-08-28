---
title: Network.bufferingProgress
description: La propiedad bufferingProgress recupera el porcentaje de almacenamiento en búfer completado.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Network.bufferingProgress Reproductor de Windows Media
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
ms.openlocfilehash: 65de3f7b1b58dfb90f76436f324dcc3d4fc3fe9a24b7c60ca3db888771f9192d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901755"
---
# <a name="networkbufferingprogress"></a>Network.bufferingProgress

La **propiedad bufferingProgress** recupera el porcentaje de almacenamiento en búfer completado.

## <a name="syntax"></a>Syntax

*player*. *network*. **bufferingProgress**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Cada vez que se detiene y reinicia la reproducción, esta propiedad se establece en cero. No se restablece si la reproducción está en pausa.

El almacenamiento en búfer solo se aplica al contenido de streaming. Esta propiedad devuelve información válida solo durante el tiempo de ejecución, cuando el *reproductor .* **Se establece** la propiedad URL.

Use el *evento Player*.*:Buffering** para determinar cuándo se inicia o se detiene el almacenamiento en búfer.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **bufferingProgress para** mostrar el porcentaje de almacenamiento en búfer completado. La información se muestra en una DIV HTML creada con id. = "BP". En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player.Buffering (Evento)**](player-player-buffering.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





