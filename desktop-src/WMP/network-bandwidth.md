---
title: Red. ancho de banda
description: La propiedad de ancho de banda recupera el ancho de banda actual del clip.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Red. ancho de banda Media Player Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708641"
---
# <a name="networkbandwidth"></a>Red. ancho de banda

La propiedad de **ancho** de banda recupera el ancho de banda actual del clip.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **ancho de banda**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve cero si el *reproductor*. La propiedad de **dirección URL** no está establecida. Esta propiedad solo es válida para streaming multimedia.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de Microsoft JScript se usa *Network*. **ancho de banda** para mostrar el ancho de banda multimedia actual. La información se muestra en un DIV HTML creado con ID = "BW". El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





