---
title: Atributo AverageLevel
description: El atributo AverageLevel es un valor de amplitud de 16 bits que indica el nivel medio del volumen.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- Atributo AverageLevel Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e169b1e2d63e6f8215515acc852d431ff13ccd513924e4c2a237b16c17dacfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582750"
---
# <a name="averagelevel-attribute"></a>Atributo AverageLevel

El **atributo AverageLevel** es un valor de amplitud de 16 bits que indica el nivel medio del volumen.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Archivos multimedia de Windows usados con frecuencia](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

Reproductor de Windows Media establece este valor en cualquiera de las siguientes instancias:

-   Después de que haya arrancado un archivo.
-   Después de reproducir un archivo (cuando está habilitada la mejora de nivelación automática de volumen).

La Windows DEL SDK de formato multimedia para este atributo es g \_ wszAverageLevel.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





