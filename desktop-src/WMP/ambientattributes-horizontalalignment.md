---
title: AmbientAttributes. horizontalAlignment
description: El atributo horizontalAlignment especifica o recupera un valor que indica la posición horizontal del control cuando se cambia el tamaño de la vista o la subvista primaria.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- AmbientAttributes. horizontalAlignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698635"
---
# <a name="ambientattributeshorizontalalignment"></a>AmbientAttributes. horizontalAlignment

El atributo **horizontalAlignment** especifica o recupera un valor que indica la posición horizontal del control cuando se cambia el **tamaño de la vista o la** **subvista** primaria.

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.



| Value   | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| izquierda    | Predeterminada. Mantiene la posición del control en relación con la parte izquierda de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                               |
| right   | Mantiene la posición del control en relación con la derecha de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                                       |
| centro  | Mantiene la posición del control en relación con el centro horizontal de la **vista** o la **subvista** primaria cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                           |
| ajustar | Mantiene la posición del control en relación con los márgenes izquierdo y derecho de la **vista** o la **subvista** primaria cuando se cambia el tamaño. El control se ajusta para ajustarse cuando se ajusta la **vista** o la **subvista** . La imagen real no aumenta ni se reduce a menos que se puedan cambiar de tamaño, pero el área en la que se hace clic aumenta o disminuye si no está limitada por un **clippingImage**. |



 

## <a name="remarks"></a>Observaciones

A menos que **horizontalAlignment** se establezca en "Center", el control conserva su distancia original desde el borde especificado o desde ambos bordes si se especifica "stretch" y se ajusta el tamaño del control. Si el control no es de tamaño variable y se especifica "stretch", en su lugar se expande la región en la que se hace clic.

Puede establecer cualquier combinación de **horizontalAlignment** y **verticalAlignment**. Por ejemplo, si desea centrar un control tanto horizontal como verticalmente, establezca horizontalAlignment = "Center" verticalAlignment = "Center".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. verticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





