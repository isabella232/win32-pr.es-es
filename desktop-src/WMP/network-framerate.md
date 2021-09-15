---
title: Network.frameRate
description: La propiedad frameRate recupera la velocidad de fotogramas de vídeo actual en fotogramas por cien segundos. Por ejemplo, un valor de 2998 indica 29,98 fotogramas por segundo.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Network.frameRate Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473334"
---
# <a name="networkframerate"></a>Network.frameRate

La **propiedad frameRate** recupera la velocidad de fotogramas de vídeo actual en fotogramas por cien segundos. Por ejemplo, un valor de 2998 indica 29,98 fotogramas por segundo.

## <a name="syntax"></a>Sintaxis

*player*. *network*. **frameRate**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **frameRate** para mostrar la velocidad de fotogramas actual. La información se muestra en una DIV HTML creada con id. = "FR". El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
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
</dt> <dt>

[**Network.encodedFrameRate**](network-encodedframerate.md)
</dt> </dl>

 

 





