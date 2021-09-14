---
title: BUTTONGROUP.showBackground
description: El atributo showBackground especifica o recupera un valor que indica si BUTTONGROUP muestra solo los botones o muestra el mapa de bits completo especificado en el atributo image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- ButtonGROUP.showBackground Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889260"
---
# <a name="buttongroupshowbackground"></a>BUTTONGROUP.showBackground

El **atributo showBackground** especifica o recupera un valor que indica si **BUTTONGROUP** muestra solo los botones o muestra el mapa de bits completo especificado en el **atributo image.**

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Se muestran botones y el área no ocupada por los botones se dibuja desde el mapa de bits Imagen. |
| false | Predeterminada. Solo se muestran los botones.                                                   |



 

## <a name="remarks"></a>Observaciones

Cuando **showBackground** es true, toda la imagen **principal** estará visible.

Cuando **showBackground** es false, solo se representarán las áreas correspondientes a **mappingImage** colors asignadas. En otras palabras, solo estarán visibles **los BUTTONELEMENTs** con **su mappingColor** asignado.

Si se especifica un valor no válido, se mantiene el estado anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





