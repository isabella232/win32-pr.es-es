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
ms.openlocfilehash: c4d40d1933c68c4e34707f01a4d425045c773297e8567ba8ea13a88c6fbc57c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749466"
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



 

## <a name="remarks"></a>Comentarios

Este atributo solo se puede establecer en "contraseña" o "multilínea" en tiempo de diseño. Si se establece en "multilínea", el valor no se puede cambiar en tiempo de ejecución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> </dl>

 

 





