---
title: AmbientAttributes.horizontalAlignment
description: El atributo horizontalAlignment especifica o recupera un valor que indica la posición horizontal del control cuando se cambia el tamaño de LA VISTA o subvista primaria.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- AmbientAttributes.horizontalAlignment Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889969"
---
# <a name="ambientattributeshorizontalalignment"></a>AmbientAttributes.horizontalAlignment

El **atributo horizontalAlignment** especifica o recupera un valor que indica la posición horizontal del control cuando se cambia el tamaño de **LA** VISTA o **subvista** primaria.

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**



| Value   | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| izquierda    | Predeterminada. Mantiene la posición del control con respecto a la izquierda de **VIEW** o **SUBVIEW primaria** cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                               |
| right   | Mantiene la posición del control en relación con la derecha de **VIEW** o **SUBVIEW primaria** cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                                       |
| centro  | Mantiene la posición del control en relación con el centro horizontal de **VIEW** o **SUBVIEW primario** cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                           |
| ajustar | Mantiene la posición del control en relación con los márgenes izquierdo y derecho de **VIEW** o **SUBVIEW primario** cuando se cambia el tamaño. El control se ajusta para ajustarse **cuando** se ajusta view o **SUBVIEW.** La imagen real no crece ni se reduce a menos que sea ajustable, pero el área en la que se puede hacer clic crece o se reduce si no está limitada por **un clippingImage**. |



 

## <a name="remarks"></a>Observaciones

A menos **que horizontalAlignment** se establezca en "center", el control conserva su distancia original desde el borde especificado o desde ambos bordes si se especifica "stretch" y el control se puede cambiar de tamaño. Si el control no es ajustable y se especifica "stretch", la región en la que se puede hacer clic se extiende en su lugar.

Puede establecer cualquier combinación de **horizontalAlignment y** **verticalAlignment**. Por ejemplo, si desea centrar un control tanto horizontal como verticalmente, establezca horizontalAlignment="center" verticalAlignment="center".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.verticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





