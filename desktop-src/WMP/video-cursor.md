---
title: VIDEO.cursor
description: El atributo cursor especifica o recupera el valor del cursor que se usa cuando el mouse está sobre un área en la que se puede hacer clic del vídeo.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- Video.cursor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c39b40412a02e145b8063f473272184e1d7cf03caaa170de19bde7fad37a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134248"
---
# <a name="videocursor"></a>VIDEO.cursor

El **atributo** cursor especifica o recupera el valor del cursor que se usa cuando el mouse está sobre un área en la que se puede hacer clic del vídeo.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y escritura.**



| Value            | Descripción                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Cursor dependiente de la plataforma (normalmente una flecha).                                               |
| Mano             | Mano.                                                                                       |
| ayuda             | Flecha con signo de interrogación que indica que la Ayuda está disponible.                                      |
| sizeall          | Flecha de cuatro puntas que apunta al norte, sur, este y oeste.                                   |
| sizenesw         | Flecha de doble punta que apunta hacia el noreste y el suroeste.                                      |
| sizens           | Flecha de doble punta que apunta hacia el norte y el sur.                                              |
| sizenwse         | Flecha de doble punta que apunta al noroeste y al sudeste.                                      |
| sizewe           | Flecha de doble punta que apunta hacia el oeste y el este.                                                |
| arriba          | Flecha vertical que apunta hacia arriba.                                                             |
| \*.ani o \* .cur | Cualquier archivo .ani o .cur (debe estar en el mismo directorio que el archivo .wms o en el archivo .wmz). |



 

## <a name="remarks"></a>Comentarios

Con fines de representación, el sistema es el cursor predeterminado. El valor predeterminado recuperado de este atributo es "" (cadena vacía).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> </dl>

 

 





