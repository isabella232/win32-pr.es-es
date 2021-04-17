---
title: AmbientAttributes. verticalAlignment
description: El atributo verticalAlignment especifica o recupera un valor que indica la posición vertical del control cuando se ajusta la vista o la subvista primaria.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- AmbientAttributes. verticalAlignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700193"
---
# <a name="ambientattributesverticalalignment"></a>AmbientAttributes. verticalAlignment

El atributo **verticalAlignment** especifica o recupera un valor que indica la posición vertical del control cuando se ajusta la **vista** o la **subvista** primaria.

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.



| Value   | Descripción                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| top     | Predeterminada. Mantiene la posición del control en relación con la parte superior de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.                                                                                                                                                                                                             |
| abajo  | Mantiene la posición del control en relación con la parte inferior de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                   |
| centro  | Mantiene la posición del control en relación con el centro vertical de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.                                                                                                                                                                                                          |
| ajustar | Mantiene la posición del control en relación con los márgenes superior e inferior de la vista cuando se cambia el tamaño. El control se ajusta para ajustarse cuando se ajusta la **vista** o la **subvista** primaria. La imagen real no aumenta ni se reduce a menos que se puedan cambiar de tamaño, pero el área en la que se hace clic aumenta o disminuye si no está limitada por un **clippingImage**. |



 

## <a name="remarks"></a>Observaciones

A menos que **verticalAlignment** se establezca en "Center", el control conserva su distancia original desde el borde especificado o desde ambos bordes si se especifica "stretch" y se ajusta el tamaño del control. Si el control no es de tamaño variable y se especifica "stretch", en su lugar se expande la región en la que se hace clic.

Puede establecer cualquier combinación de los atributos **horizontalAlignment** y **verticalAlignment** . Por ejemplo, si desea que un control se Centre tanto horizontal como verticalmente, establezca **horizontalAlignment** en "Center" y **verticalAlignment** en "Center".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. horizontalAlignment**](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





