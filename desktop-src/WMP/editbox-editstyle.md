---
title: EDITBOX.editStyle
description: El atributo editStyle especifica o recupera el estilo del control de cuadro de edición.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- EDITBOX.editStyle Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068444"
---
# <a name="editboxeditstyle"></a>EDITBOX.editStyle

El **atributo editStyle** especifica o recupera el estilo del control de cuadro de edición.

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene uno de los valores siguientes.



| Value     | Descripción                                                                     |
|-----------|---------------------------------------------------------------------------------|
| normal    | Predeterminada. Muestra texto normal en una sola línea.                                 |
| password  | Muestra asteriscos ( \* ) en lugar de texto. Solo se puede especificar en tiempo de diseño. |
| mayúsculas | Muestra el texto en mayúsculas.                                                 |
| minúsculas | Muestra el texto en minúsculas.                                                 |
| number    | Solo muestra números.                                                          |
| Multilínea | Muestra varias líneas de texto. Solo se puede especificar en tiempo de diseño.          |



 

## <a name="remarks"></a>Observaciones

Este atributo solo se puede establecer en "contraseña" o "multilínea" en tiempo de diseño. Si se establece en "multilínea", el valor no se puede cambiar en tiempo de ejecución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> </dl>

 

 





