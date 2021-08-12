---
title: Atributo PeakValue
description: El atributo PeakValue es un valor de amplitud de 16 bits que indica el nivel de volumen máximo.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Atributo PeakValue Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a661342b305155717f4f11336f540e1ae53524ff2d303a2ab790e2c73af7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573589"
---
# <a name="peakvalue-attribute"></a>Atributo PeakValue

El **atributo PeakValue** es un valor de amplitud de 16 bits que indica el nivel de volumen máximo.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Archivos multimedia de Windows usados con frecuencia](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

Reproductor de Windows Media establece este valor en cualquiera de las instancias siguientes:

-   Después de que haya arrancado un archivo.
-   Después de reproducir un archivo (cuando está habilitada la mejora de nivelación automática de volumen).

La Windows SDK de formato multimedia para este atributo es g \_ wszPeakValue.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





