---
title: Network.bitRate
description: La propiedad bitRate recupera la velocidad de bits actual que se recibe.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Network.bitRate Reproductor de Windows Media
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
ms.openlocfilehash: ec142885bdd718903e956f8e86b59c3753cb024ecccc5efb2f8494797ea6a818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901785"
---
# <a name="networkbitrate"></a>Network.bitRate

La **propiedad bitRate** recupera la velocidad de bits actual que se recibe.

## <a name="syntax"></a>Syntax

*player*. *red*. **bitRate**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Este valor es una combinación de las velocidades de bits de las secuencias de audio y vídeo actuales.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **bitRate** para mostrar la velocidad de bits del medio actual. La información se muestra en un DIV HTML creado con id. = "BR". El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





