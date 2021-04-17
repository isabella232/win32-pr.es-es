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
# <a name="networkreceivedpackets"></a>Network. receivedPackets

La propiedad **receivedPackets** recupera el número de paquetes recibidos.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **receivedPackets**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="remarks"></a>Observaciones

Cada vez que se detiene y se reinicia la reproducción de un clip, esta propiedad se establece en cero. No se restablece si la reproducción de archivos está en pausa.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **receivedPackets** para mostrar el número de paquetes recibidos. La información se muestra en un DIV HTML creado con ID = "RP". En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla. El objeto **Player** se creó con ID = "Player".


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





