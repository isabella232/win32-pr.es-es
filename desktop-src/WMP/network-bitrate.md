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
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967423"
---
# <a name="networkbitrate"></a>Network.bitRate

La **propiedad bitRate** recupera la velocidad de bits actual que se recibe.

## <a name="syntax"></a>Sintaxis

*player*. *network*. **bitRate**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Observaciones

Este valor es una combinación de las velocidades de bits de las secuencias de audio y vídeo actuales.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **bitRate** para mostrar la velocidad de bits del medio actual. La información se muestra en una DIV HTML creada con id. = "BR". El **objeto Player** se creó con id. = "Player".


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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





