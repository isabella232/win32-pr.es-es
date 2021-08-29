---
title: LISTBOX.fontFace
description: El atributo fontFace especifica o recupera la fuente del control de cuadro de lista.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- LISTBOX.fontFace Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cf9eb2f1377a92e83d3bc27f8c9491a50369a317af19d16eb2bde765f70958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054703"
---
# <a name="listboxfontface"></a>LISTBOX.fontFace

El **atributo fontFace** especifica o recupera la fuente del control de cuadro de lista.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Comentarios

Este atributo puede ser el nombre de cualquier fuente válida disponible en Windows. Reproductor de Windows Media admitirá la instalación de fuentes, así que elija una fuente que sepa que estará en el sistema previsto.

Si el **fontFace** especificado no está disponible en el sistema del usuario, el control de cuadro de lista tiene como valor predeterminado la Windows del sistema. El valor predeterminado para los sistemas en inglés es "Glioma". Para los sistemas internacionales, el valor predeterminado se carga desde un archivo de recursos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**LISTBOX.fontSize**](listbox-fontsize.md)
</dt> <dt>

[**LISTBOX.fontStyle**](listbox-fontstyle.md)
</dt> </dl>

 

 





