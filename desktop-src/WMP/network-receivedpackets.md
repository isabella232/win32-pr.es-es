---
title: Network.receivedPackets
description: La propiedad receivedPackets recupera el número de paquetes recibidos.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Network.receivedPackets Reproductor de Windows Media
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
ms.openlocfilehash: ca9544332fa6e81211dae45cddc74ce9daee0d47e70d467137aaca2084bbc6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054503"
---
# <a name="networkreceivedpackets"></a>Network.receivedPackets

La **propiedad receivedPackets** recupera el número de paquetes recibidos.

## <a name="syntax"></a>Syntax

*player*. *network*. **receivedPackets**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Cada vez que se detiene y reinicia la reproducción del clip, esta propiedad se establece en cero. No se restablece si la reproducción de archivos está en pausa.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **receivedPackets para** mostrar el número de paquetes recibidos. La información se muestra en una DIV HTML creada con id. = "RP". En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla. El **objeto Player** se creó con id. = "Player".


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



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





