---
title: Atributo PeakValue
description: El atributo PeakValue es un valor de amplitud de 16 bits que indica el nivel de volumen máximo.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- PeakValue Media Player de Windows
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700256"
---
# <a name="peakvalue-attribute"></a>Atributo PeakValue

El atributo **PeakValue** es un valor de amplitud de 16 bits que indica el nivel de volumen máximo.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Archivos de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

Windows Media Player establece este valor en cualquiera de las instancias siguientes:

-   Una vez que haya copiado un archivo.
-   Una vez que haya reproducido un archivo (cuando la mejora de la nivelación de volumen automática está habilitada).

La constante del SDK de Windows Media Format para este atributo es g \_ wszPeakValue.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





