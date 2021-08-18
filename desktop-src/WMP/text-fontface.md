---
title: TEXT.fontFace
description: El atributo fontFace especifica o recupera el tipo de letra para el control Text.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- TEXT.fontFace Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b1044d01ac3ca6a8cc4f1212232bfcc630eb73831f90eb7fd5f423f5dc38d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118366"
---
# <a name="textfontface"></a>TEXT.fontFace

El **atributo fontFace** especifica o recupera el tipo de letra para el control Text.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Comentarios

Este atributo puede ser el nombre de cualquier fuente válida disponible en Windows. Reproductor de Windows Media admitirá la instalación de fuentes, así que elija una fuente que sepa que estará en el sistema previsto.

Si la **fontFace** especificada no está disponible en el sistema del usuario, el control Texto tiene como valor predeterminado la Windows del sistema.

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.fontSize**](text-fontsize.md)
</dt> </dl>

 

 





