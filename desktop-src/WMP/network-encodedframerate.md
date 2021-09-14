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
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967420"
---
# <a name="networkencodedframerate"></a>Network.encodedFrameRate

La **propiedad encodedFrameRate** recupera la velocidad de fotogramas de vídeo especificada por el autor del contenido en fotogramas por segundo.

## <a name="syntax"></a>Sintaxis

*player*. *red*. **encodedFrameRate**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **encodedFrameRate** para mostrar la velocidad de fotogramas especificada cuando se codifica el archivo. La información se muestra en un DIV HTML creado con id. = "FR". El **objeto Player** se creó con id. = "Player".


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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Network.frameRate**](network-framerate.md)
</dt> </dl>

 

 





