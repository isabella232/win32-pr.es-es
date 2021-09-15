---
title: TEXT.cursor
description: El atributo cursor especifica o recupera un valor que indica qué cursor aparece cuando el mouse está sobre el control Text.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- Text.cursor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569768"
---
# <a name="textcursor"></a>TEXT.cursor

El **atributo** cursor especifica o recupera un valor que indica qué cursor aparece cuando el mouse está sobre el control Text.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y escritura.**



| Value            | Descripción                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Predeterminada. Cursor dependiente de la plataforma (normalmente una flecha).                                      |
| Mano             | Mano.                                                                                       |
| help             | Flecha con signo de interrogación que indica que la Ayuda está disponible.                                      |
| sizeall          | Flecha de cuatro puntas que apunta al norte, sur, este y oeste.                                   |
| sizenesw         | Flecha de doble punta que apunta hacia el noreste y el suroeste.                                      |
| sizens           | Flecha de doble punta que apunta hacia el norte y el sur.                                              |
| sizenwse         | Flecha de doble punta que apunta al noroeste y al sudeste.                                      |
| sizewe           | Flecha de doble punta que apunta hacia el oeste y el este.                                                |
| arriba          | Flecha vertical que apunta hacia arriba.                                                             |
| \*.ani o \* .cur | Cualquier archivo .ani o .cur (debe estar en el mismo directorio que el archivo .wms o en el archivo .wmz). |



 

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





