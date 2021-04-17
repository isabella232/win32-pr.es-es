---
title: EDITBOX. editStyle
description: El atributo editStyle especifica o recupera el estilo del control de cuadro de edición.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- EditStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699877"
---
# <a name="editboxeditstyle"></a>EDITBOX. editStyle

El atributo **editStyle** especifica o recupera el estilo del control de cuadro de edición.

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene uno de los valores siguientes.



| Value     | Descripción                                                                     |
|-----------|---------------------------------------------------------------------------------|
| normal    | Predeterminada. Muestra el texto normal en una sola línea.                                 |
| password  | Muestra asteriscos ( \* ) en lugar de texto. Solo se puede especificar en tiempo de diseño. |
| mayúsculas | Muestra el texto en mayúsculas.                                                 |
| minúsculas | Muestra el texto en minúsculas.                                                 |
| number    | Solo muestra los números.                                                          |
| ocupa | Muestra varias líneas de texto. Solo se puede especificar en tiempo de diseño.          |



 

## <a name="remarks"></a>Observaciones

Este atributo solo se puede establecer en "Password" o "Multiline" en tiempo de diseño. Si se establece en "Multiline", no se puede cambiar el valor en tiempo de ejecución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> </dl>

 

 





