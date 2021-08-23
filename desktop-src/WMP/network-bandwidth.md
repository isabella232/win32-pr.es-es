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
ms.openlocfilehash: 40bd97ae2efe7513bc69d308a29356cfc7b141ecc84b816bdc7fad68d79aa785
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616882"
---
# <a name="networkbandwidth"></a>Network.bandWidth

La **propiedad bandWidth** recupera el ancho de banda actual del clip.

## <a name="syntax"></a>Syntax

*player*. *network*. **bandWidth**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve cero si *player*. **La propiedad URL** no está establecida. Esta propiedad solo es válida para los medios de streaming.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo JScript de Microsoft se usa *Network*. **bandWidth para** mostrar el ancho de banda de medios actual. La información se muestra en una DIV HTML creada con id. = "BW". El **objeto Player** se creó con id. = "Player".


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



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





