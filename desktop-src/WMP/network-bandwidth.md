---
title: Network.bandWidth
description: La propiedad bandWidth recupera el ancho de banda actual del clip.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Network.bandWidth Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967431"
---
# <a name="networkbandwidth"></a>Network.bandWidth

La **propiedad bandWidth** recupera el ancho de banda actual del clip.

## <a name="syntax"></a>Sintaxis

*player*. *red*. **bandWidth**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve cero si *player*. **La propiedad URL** no está establecida. Esta propiedad solo es válida para los medios de streaming.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo JScript microsoft usa *Network*. **bandWidth para** mostrar el ancho de banda de medios actual. La información se muestra en un DIV HTML creado con id. = "BW". El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
}
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





