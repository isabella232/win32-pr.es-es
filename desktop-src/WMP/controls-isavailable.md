---
title: Controls.isAvailable
description: La propiedad isAvailable indica si un tipo de información especificado está disponible o se puede realizar una acción especificada. | Controls.isAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Controls.isAvailable Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502343b7654241a00e9efb33acc6f5de842c6fb6bad650f24839a5fe7febf9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135748"
---
# <a name="controlsisavailable"></a>Controls.isAvailable

La **propiedad isAvailable** indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parámetros

*name*

**Cadena** que contiene uno de los valores siguientes.



| String          | Descripción                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Currentitem     | Determina si el usuario puede establecer la **propiedad currentItem.**                                                                                                 |
| currentMarker   | Determina si el usuario puede buscar un marcador específico.                                                                                                        |
| currentPosition | Determina si el usuario puede buscar una posición específica en el archivo. Algunos archivos no admiten búsquedas.                                                       |
| fastForward     | Determina si el archivo admite el reenvío rápido y si se puede invocar esa funcionalidad. Muchos tipos de archivo (o transmisiones en vivo) no admiten fastForward. |
| fastReverse     | Determina si el archivo admite fastReverse y si se puede invocar esa funcionalidad. Muchos tipos de archivo (o transmisiones en vivo) no admiten fastReverse.     |
| Siguiente            | Determina si el usuario puede buscar a la siguiente entrada de una lista de reproducción.                                                                                             |
| pause           | Determina si el método **pause** está disponible.                                                                                                             |
| Jugar            | Determina si el **método de reproducción** está disponible.                                                                                                              |
| previous        | Determina si el usuario puede buscar la entrada anterior en una lista de reproducción.                                                                                         |
| paso            | Determina si el método **step** está disponible durante la reproducción.                                                                                              |
| stop            | Determina si el **método stop** está disponible.                                                                                                              |



 

## <a name="return-values"></a>Valores devueltos

Este método devuelve un **valor booleano.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que busca en la posición inicial del elemento multimedia actual. El JScript usa **isAvailable para** comprobar que el archivo admite la operación de búsqueda. El **objeto Player** se creó con id. = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/>                               |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> </dl>

 

 





