---
title: AmbientAttributes.verticalAlignment
description: El atributo verticalAlignment especifica o recupera un valor que indica la posición vertical del control cuando se extiende la vista o subvista primaria.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- AmbientAttributes.verticalAlignment Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889929"
---
# <a name="ambientattributesverticalalignment"></a>AmbientAttributes.verticalAlignment

El **atributo verticalAlignment** especifica o recupera un valor que indica la posición vertical del control cuando se extiende la **vista** o **subvista** primaria.

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y escritura.**



| Value   | Descripción                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| top     | Predeterminada. Mantiene la posición del control con respecto a la parte superior de **VIEW** o **SUBVIEW primaria** cuando se cambia el tamaño de la vista.                                                                                                                                                                                                             |
| abajo  | Mantiene la posición del control en relación con la parte inferior de **VIEW** o **SUBVIEW primaria** cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                   |
| centro  | Mantiene la posición del control en relación con el centro vertical de **LA VISTA** o **subvista primaria** cuando se cambia el tamaño de la vista.                                                                                                                                                                                                          |
| ajustar | Mantiene la posición del control en relación con los márgenes superior e inferior de la vista cuando se cambia el tamaño. El control se ajusta para ajustarse cuando se ajusta la **vista** o **subvista** primaria. La imagen real no crece ni se reduce a menos que sea de tamaño ajustable, pero el área en la que se puede hacer clic crece o se reduce si no está delimitada por **un recorteImage .** |



 

## <a name="remarks"></a>Observaciones

A menos **que verticalAlignment** se establezca en "center", el control conserva su distancia original desde el borde especificado, o desde ambos bordes si se especifica "stretch" y se puede cambiar el tamaño del control. Si el control no es ajustable y se especifica "stretch", la región en la que se puede hacer clic se extiende en su lugar.

Puede establecer cualquier combinación de los **atributos horizontalAlignment** y **verticalAlignment.** Por ejemplo, si desea que un control se centre horizontal y verticalmente, establezca **horizontalAlignment** en "center" y **verticalAlignment** en "center".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.horizontalAlignment**](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





