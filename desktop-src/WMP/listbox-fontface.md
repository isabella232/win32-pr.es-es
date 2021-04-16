---
title: LISTBOX. fontFace
description: El atributo fontFace especifica o recupera la fuente para el control de cuadro de lista.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- LISTBOX. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699637"
---
# <a name="listboxfontface"></a>LISTBOX. fontFace

El atributo **fontFace** especifica o recupera la fuente para el control de cuadro de lista.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Este atributo puede ser el nombre de cualquier fuente válida disponible en Windows. Windows Media Player no admitirá la instalación de fuentes, así que elija una fuente que sepa que se encuentra en el sistema previsto.

Si el **fontFace** especificado no está disponible en el sistema del usuario, el control de cuadro de lista tiene como valor predeterminado la fuente del sistema de Windows. El valor predeterminado para los sistemas en inglés es "Tahoma". En el caso de los sistemas internacionales, el valor predeterminado se carga desde un archivo de recursos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**LISTBOX. FontSize**](listbox-fontsize.md)
</dt> <dt>

[**LISTBOX. fontStyle**](listbox-fontstyle.md)
</dt> </dl>

 

 





