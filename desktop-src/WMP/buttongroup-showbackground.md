---
title: BUTTONGROUP.showBackground
description: El atributo showBackground especifica o recupera un valor que indica si el BUTTONGROUP muestra solo los botones o muestra el mapa de bits completo especificado en el atributo de imagen.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- BUTTONGROUP. showBackground Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699518"
---
# <a name="buttongroupshowbackground"></a>BUTTONGROUP.showBackground

El atributo **showBackground** especifica o recupera un valor que indica si el **BUTTONGROUP** muestra solo los botones o muestra el mapa de bits completo especificado en el atributo de **imagen** .

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Se muestran los botones y el área no ocupada por los botones se dibuja desde el mapa de bits de la imagen. |
| false | Predeterminada. Solo se muestran los botones.                                                   |



 

## <a name="remarks"></a>Observaciones

Cuando **showBackground** es true, toda la **imagen** principal será visible.

Cuando **showBackground** es false, solo se representarán las áreas correspondientes a los colores **mappingImage** asignados. En otras palabras, solo estarán visibles los **BUTTONELEMENTs** con sus **mappingColor** asignados.

Si se especifica un valor no válido, se mantiene el estado anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONELEMENT. mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP. Image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





