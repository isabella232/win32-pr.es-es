---
title: Red. velocidad de fotogramas
description: La propiedad de velocidad de fotogramas recupera la velocidad actual de fotogramas de vídeo en fotogramas por cien segundos. Por ejemplo, un valor de 2998 indica 29,98 fotogramas por segundo.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Red. velocidad de Media Player de Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708972"
---
# <a name="networkframerate"></a>Red. velocidad de fotogramas

La propiedad de **velocidad** de fotogramas recupera la velocidad actual de fotogramas de vídeo en fotogramas por cien segundos. Por ejemplo, un valor de 2998 indica 29,98 fotogramas por segundo.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **velocidad de fotograma**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **velocidad de** fotogramas para mostrar la velocidad de fotogramas actual. La información se muestra en un DIV HTML creado con ID = "FR". El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Network. encodedFrameRate**](network-encodedframerate.md)
</dt> </dl>

 

 





