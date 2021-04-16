---
title: Atributo AverageLevel
description: El atributo AverageLevel es un valor de amplitud de 16 bits que indica el nivel de volumen medio.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- AverageLevel Media Player de Windows
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699426"
---
# <a name="averagelevel-attribute"></a>Atributo AverageLevel

El atributo **AverageLevel** es un valor de amplitud de 16 bits que indica el nivel de volumen medio.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Archivos de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

Windows Media Player establece este valor en cualquiera de las instancias siguientes:

-   Una vez que haya copiado un archivo.
-   Una vez que haya reproducido un archivo (cuando la mejora de la nivelación de volumen automática está habilitada).

La constante del SDK de Windows Media Format para este atributo es g \_ wszAverageLevel.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





