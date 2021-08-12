---
title: Network.receptionQuality
description: La propiedad receivedQuality recupera el porcentaje de paquetes recibidos en los últimos 30 segundos.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Network.receptionQuality Reproductor de Windows Media
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
ms.openlocfilehash: 159bcac192d5a5bd9197ecc3ea935027dd6d707dde42a54c64a318459ae00040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574161"
---
# <a name="networkreceptionquality"></a>Network.receptionQuality

La **propiedad receivedQuality** recupera el porcentaje de paquetes recibidos en los últimos 30 segundos.

## <a name="syntax"></a>Syntax

*player*. *red*. **receptionQuality**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

El número de paquetes recibidos, perdidos y recuperados durante el streaming se supervisa una vez cada segundo. **receptionQuality es** el porcentaje de paquetes que no se pierden durante los últimos 30 segundos.

Cada vez que se detiene y reinicia la reproducción, esta propiedad se establece en cero. No se restablece si la reproducción está en pausa.

Esta propiedad devuelve información válida solo durante el tiempo de ejecución y solo si el *reproductor .* **También se** establece la propiedad URL.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **receivedQuality para** mostrar el porcentaje de paquetes recibidos. La información se muestra en un DIV HTML creado con id. = "RQ". En el ejemplo se usa un temporizador con un intervalo de 30 segundos para actualizar la pantalla. El **objeto Player** se creó con id. = "Player".


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





