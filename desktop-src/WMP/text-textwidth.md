---
title: TEXT. textWidth
description: El atributo textWidth recupera el ancho en píxeles del texto contenido en el atributo value.
ms.assetid: 46c34659-f441-467c-8846-45785f7a2736
keywords:
- Media Player de Windows TEXT. textWidth
topic_type:
- apiref
api_name:
- TEXT.textWidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17ce93517837aecf737336137df3cf5d8bf292dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708906"
---
# <a name="texttextwidth"></a>TEXT. textWidth

El atributo **textWidth** recupera el ancho en píxeles del texto contenido en el atributo **Value** .

``` syntax
        elementID.textWidth
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de solo lectura (**int**).

## <a name="remarks"></a>Observaciones

El valor devuelto se basa en los atributos **fontFace**, **FontSize** y **fontStyle** , así como en los caracteres reales de la cadena de atributo **Value** .

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT. fontFace**](text-fontface.md)
</dt> <dt>

[**TEXT. FontSize**](text-fontsize.md)
</dt> <dt>

[**TEXT. fontStyle**](text-fontstyle.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> </dl>

 

 





