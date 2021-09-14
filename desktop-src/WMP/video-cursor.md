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
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070833"
---
# <a name="videocursor"></a>VIDEO.cursor

El **atributo** cursor especifica o recupera el valor del cursor que se usa cuando el mouse está sobre un área en la que se puede hacer clic del vídeo.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**



| Value            | Descripción                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Cursor dependiente de la plataforma (normalmente una flecha).                                               |
| Mano             | Mano.                                                                                       |
| help             | Flecha con signo de interrogación que indica que la Ayuda está disponible.                                      |
| sizeall          | Flecha de cuatro puntas que apunta al norte, sur, este y oeste.                                   |
| sizenesw         | Flecha de doble punta que apunta hacia el nordeste y el suroeste.                                      |
| sizens           | Flecha de doble punta que apunta hacia el norte y el sur.                                              |
| sizenwse         | Flecha de doble punta que apunta al sudeste y al sudeste.                                      |
| sizewe           | Flecha de doble punta que apunta hacia el oeste y el este.                                                |
| uparrow          | Flecha vertical que apunta hacia arriba.                                                             |
| \*.ani o \* .cur | Cualquier archivo .ani o .cur (debe estar en el mismo directorio que el archivo .wms o en el archivo .wmz). |



 

## <a name="remarks"></a>Observaciones

Con fines de representación, el sistema es el cursor predeterminado. El valor predeterminado recuperado de este atributo es "" (cadena vacía).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> </dl>

 

 





