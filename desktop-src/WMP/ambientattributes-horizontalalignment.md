---
title: AmbientAttributes.horizontalAlignment
description: El atributo horizontalAlignment especifica o recupera un valor que indica la posición horizontal del control cuando se cambia el tamaño de view o subview primario.
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
ms.openlocfilehash: 9daf64189735d79e1ad3eb4f7b3637ca68cfdae489cda9423bb60acdd1f9185c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055173"
---
# <a name="ambientattributeshorizontalalignment"></a>AmbientAttributes.horizontalAlignment

El **atributo horizontalAlignment** especifica o recupera un valor que indica la posición horizontal del control cuando se cambia el tamaño de **view** o **subview** primario.

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y escritura.**



| Valor   | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| izquierda    | Predeterminada. Mantiene la posición del control con respecto a la izquierda de **VIEW** o **SUBVIEW primaria** cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                               |
| right   | Mantiene la posición del control en relación con la derecha de **VIEW** o **SUBVIEW primaria** cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                                       |
| centro  | Mantiene la posición del control en relación con el centro horizontal de **LA VISTA** o **subvista primaria** cuando se cambia el tamaño de la vista.                                                                                                                                                                                                                           |
| ajustar | Mantiene la posición del control en relación con los márgenes izquierdo y derecho de **VIEW** o **SUBVIEW principal** cuando se cambia el tamaño. El control se ajusta para ajustarse cuando se ajusta **view** o **SUBVIEW.** La imagen real no crece ni se reduce a menos que sea de tamaño ajustable, pero el área en la que se puede hacer clic crece o se reduce si no está delimitada por **un recorteImage .** |



 

## <a name="remarks"></a>Comentarios

A menos que **horizontalAlignment** se establezca en "center", el control conserva su distancia original desde el borde especificado o desde ambos bordes si se especifica "stretch" y se puede cambiar el tamaño del control. Si el control no es ajustable y se especifica "stretch", la región en la que se puede hacer clic se extiende en su lugar.

Puede establecer cualquier combinación de **horizontalAlignment** y **verticalAlignment**. Por ejemplo, si desea centrar un control tanto horizontal como verticalmente, establezca horizontalAlignment="center" verticalAlignment="center".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.verticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





