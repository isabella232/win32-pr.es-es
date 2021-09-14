---
title: EDITBOX.fontFace
description: El atributo fontFace especifica o recupera la fuente del texto en el control de cuadro de edición.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- EDITBOX.fontFace Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241071"
---
# <a name="editboxfontface"></a>EDITBOX.fontFace

El **atributo fontFace** especifica o recupera la fuente del texto en el control de cuadro de edición.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Observaciones

Este atributo puede ser el nombre de cualquier fuente válida disponible en Windows. Reproductor de Windows Media admitirá la instalación de fuentes, así que elija una fuente que sepa que estará en el sistema previsto.

Si el **fontFace** especificado no está disponible en el sistema del usuario, el control de cuadro de edición tiene como valor predeterminado la Windows del sistema. El valor predeterminado para los sistemas en inglés es "Glioma". Para los sistemas internacionales, el valor predeterminado se carga desde un archivo de recursos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.fontSize**](editbox-fontsize.md)
</dt> <dt>

[**EDITBOX.fontStyle**](editbox-fontstyle.md)
</dt> </dl>

 

 





