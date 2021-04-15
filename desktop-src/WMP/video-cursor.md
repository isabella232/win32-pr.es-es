---
title: VÍDEO. cursor
description: El atributo cursor especifica o recupera el valor del cursor que se utiliza cuando el mouse está sobre un área en la que se hace clic del vídeo.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- VÍDEO. cursor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709022"
---
# <a name="videocursor"></a>VÍDEO. cursor

El atributo **cursor** especifica o recupera el valor del cursor que se utiliza cuando el mouse está sobre un área en la que se hace clic del vídeo.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.



| Value            | Descripción                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Cursor dependiente de la plataforma (normalmente una flecha).                                               |
| casilla             | Casilla.                                                                                       |
| help             | Flecha con signo de interrogación que indica que la ayuda está disponible.                                      |
| sizeall          | Flecha de cuatro puntas que señala al norte, sur, este y oeste.                                   |
| sizenesw         | Flecha de doble punta que apunta al noreste y al suroeste.                                      |
| tamaños de           | Flecha de dos puntas que apunta al norte y al sur.                                              |
| sizenwse         | Flecha de dos puntas que apunta al noroeste y al sudeste.                                      |
| sizewe           | Flecha de dos puntas que apunta al oeste y al este.                                                |
| flecha arriba          | Flecha vertical que señala hacia arriba.                                                             |
| \*. ani o \* . cur | Cualquier archivo. ani o. cur (debe estar en el mismo directorio que el archivo. WMS o en el archivo. WMZ). |



 

## <a name="remarks"></a>Observaciones

Para fines de representación, el sistema es el cursor predeterminado. El valor predeterminado recuperado de este atributo es "" (cadena vacía).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vídeo**](video-element.md)
</dt> </dl>

 

 





