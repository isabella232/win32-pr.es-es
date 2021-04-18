---
title: EDITBOX. fontFace
description: El atributo fontFace especifica o recupera la fuente para el texto en el control de cuadro de edición.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- FontFace Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700109"
---
# <a name="editboxfontface"></a>EDITBOX. fontFace

El atributo **fontFace** especifica o recupera la fuente para el texto en el control de cuadro de edición.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Este atributo puede ser el nombre de cualquier fuente válida disponible en Windows. Windows Media Player no admitirá la instalación de fuentes, así que elija una fuente que sepa que se encuentra en el sistema previsto.

Si el **fontFace** especificado no está disponible en el sistema del usuario, el control del cuadro de edición tiene como valor predeterminado la fuente del sistema de Windows. El valor predeterminado para los sistemas en inglés es "Tahoma". En el caso de los sistemas internacionales, el valor predeterminado se carga desde un archivo de recursos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. FontSize**](editbox-fontsize.md)
</dt> <dt>

[**EDITBOX. fontStyle**](editbox-fontstyle.md)
</dt> </dl>

 

 





