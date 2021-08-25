---
title: Network.encodedFrameRate
description: La propiedad encodedFrameRate recupera la velocidad de fotogramas de vídeo especificada por el autor del contenido en fotogramas por segundo.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Network.encodedFrameRate Reproductor de Windows Media
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
ms.openlocfilehash: f1f64b6f57b4cfd0e7bc94715f80c1066ebe23a601e64c173926cf2cd9e36393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901705"
---
# <a name="networkencodedframerate"></a>Network.encodedFrameRate

La **propiedad encodedFrameRate** recupera la velocidad de fotogramas de vídeo especificada por el autor del contenido en fotogramas por segundo.

## <a name="syntax"></a>Syntax

*player*. *red*. **encodedFrameRate**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **encodedFrameRate** para mostrar la velocidad de fotogramas especificada al codificar el archivo. La información se muestra en un DIV HTML creado con id. = "FR". El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Network.frameRate**](network-framerate.md)
</dt> </dl>

 

 





