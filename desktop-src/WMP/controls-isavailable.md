---
title: Controls. isAvailable
description: La propiedad isAvailable indica si un tipo especificado de información está disponible o se puede realizar una acción especificada. | Controls. isAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Windows Media Player Controls. isAvailable
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
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699901"
---
# <a name="controlsisavailable"></a>Controls. isAvailable

La propiedad **isavailable** indica si un tipo especificado de información está disponible o se puede realizar una acción especificada.

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
| currentItem     | Determina si el usuario puede establecer la propiedad **CurrentItem** .                                                                                                 |
| currentMarker   | Determina si el usuario puede buscar un marcador específico.                                                                                                        |
| currentPosition | Determina si el usuario puede buscar una posición específica en el archivo. Algunos archivos no admiten búsquedas.                                                       |
| fastForward     | Determina si el archivo admite el reenvío rápido y si se puede invocar la funcionalidad. Muchos tipos de archivo (o secuencias en directo) no admiten fastForward. |
| fastReverse     | Determina si el archivo admite fastReverse y si se puede invocar esa funcionalidad. Muchos tipos de archivo (o secuencias en directo) no admiten fastReverse.     |
| Siguiente            | Determina si el usuario puede buscar la siguiente entrada en una lista de reproducción.                                                                                             |
| pause           | Determina si el método **PAUSE** está disponible.                                                                                                             |
| reproducción            | Determina si el método **Play** está disponible.                                                                                                              |
| previous        | Determina si el usuario puede buscar la entrada anterior en una lista de reproducción.                                                                                         |
| paso            | Determina si el método **Step** está disponible durante la reproducción.                                                                                              |
| stop            | Determina si el método de **detención** está disponible.                                                                                                              |



 

## <a name="return-values"></a>Valores devueltos

Este método devuelve un valor **booleano** .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que busca la posición inicial del elemento multimedia actual. El código JScript usa **isavailable** para comprobar que el archivo admite la operación de búsqueda. El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/>                               |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> </dl>

 

 





