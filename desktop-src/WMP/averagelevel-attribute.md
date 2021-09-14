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
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889825"
---
# <a name="averagelevel-attribute"></a>Atributo AverageLevel

El **atributo AverageLevel** es un valor de amplitud de 16 bits que indica el nivel medio del volumen.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Archivos multimedia de Windows usados habitualmente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

Reproductor de Windows Media establece este valor en cualquiera de las siguientes instancias:

-   Después de haber convertido un archivo en un archivo.
-   Después de reproducir un archivo (cuando se habilita la mejora de nivelación automática del volumen).

La Windows SDK de formato multimedia para este atributo es g \_ wszAverageLevel.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





