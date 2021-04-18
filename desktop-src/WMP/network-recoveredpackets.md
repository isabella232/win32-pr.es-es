---
title: Network. recoveredPackets
description: La propiedad recoveredPackets recupera el número de paquetes recuperados.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Windows Media Player de red. recoveredPackets
topic_type:
- apiref
api_name:
- Network.recoveredPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4222033d7e124e6ef29714bc47faf5664950fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699745"
---
# <a name="networkrecoveredpackets"></a>Network. recoveredPackets

La propiedad **recoveredPackets** recupera el número de paquetes recuperados.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **recoveredPackets**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="remarks"></a>Observaciones

Cada vez que se detiene y se reinicia la reproducción, esta propiedad se establece en cero. No se restablece si la reproducción está en pausa.

Esta propiedad devuelve información válida solo durante el tiempo de ejecución y solo si el *reproductor*. También se establece la propiedad **URL** . Será igual a cero cuando se usa el protocolo HTTP, que es sin pérdida.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **recoveredPackets** para mostrar el número de paquetes recuperados. La información se muestra en un DIV HTML creado con ID = "PR". En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla. El objeto **Player** se creó con ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdatePR()", 1000);
   }
   else{
      // Not playing; stop the timer.
      window.clearInterval(idI);
   }   
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdatePR(){
   PR.innerHTML = "";
   PR.innerHTML = "Packets recovered: " + Player.network.recoveredPackets;
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

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





