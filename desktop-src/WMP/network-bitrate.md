---
title: Red. velocidad de bits
description: La propiedad de velocidad de bits recupera la velocidad de bits actual recibida.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Red. velocidad de bits de Windows Media Player
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708639"
---
# <a name="networkbitrate"></a>Red. velocidad de bits

La propiedad de **velocidad** de bits recupera la velocidad de bits actual recibida.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **velocidad de bits**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="remarks"></a>Observaciones

Este valor es una combinación de las velocidades de bits de las secuencias de audio y vídeo actuales.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **velocidad** de bits para mostrar la velocidad de bits multimedia actual. La información se muestra en un DIV HTML creado con ID = "BR". El objeto **Player** se creó con ID = "Player".


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

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
</dt> </dl>

 

 





