---
title: Network. encodedFrameRate
description: La propiedad encodedFrameRate recupera la velocidad de fotogramas de vídeo especificada por el autor del contenido en fotogramas por segundo.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Windows Media Player de red. encodedFrameRate
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709013"
---
# <a name="networkencodedframerate"></a>Network. encodedFrameRate

La propiedad **encodedFrameRate** recupera la velocidad de fotogramas de vídeo especificada por el autor del contenido en fotogramas por segundo.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **encodedFrameRate**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **encodedFrameRate** para mostrar la velocidad de fotogramas especificada al codificar el archivo. La información se muestra en un DIV HTML creado con ID = "FR". El objeto **Player** se creó con ID = "Player".


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
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

[**Red. velocidad de fotogramas**](network-framerate.md)
</dt> </dl>

 

 





