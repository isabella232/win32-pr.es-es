---
title: TEXT. fontFace
description: El atributo fontFace especifica o recupera el tipo de letra para el control de texto.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- Media Player de Windows TEXT. fontFace
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718814"
---
# <a name="textfontface"></a>TEXT. fontFace

El atributo **fontFace** especifica o recupera el tipo de letra para el control de texto.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Este atributo puede ser el nombre de cualquier fuente válida disponible en Windows. Windows Media Player no admitirá la instalación de fuentes, así que elija una fuente que sepa que se encuentra en el sistema previsto.

Si el **fontFace** especificado no está disponible en el sistema del usuario, el control de texto tiene como valor predeterminado la fuente del sistema de Windows.

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT. FontSize**](text-fontsize.md)
</dt> </dl>

 

 





