---
title: Player.versionInfo
description: La propiedad versionInfo recupera un valor String que especifica la versión del Reproductor de Windows Media.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Player.versionInfo Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2251d610ad8a522155e37c8d416123c9d09faef5da2b4af4da75aeb745940f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995835"
---
# <a name="playerversioninfo"></a>Player.versionInfo

La **propiedad versionInfo** recupera un valor String que especifica la versión del Reproductor de Windows Media.

## <a name="syntax"></a>Syntax

*player* . **versionInfo**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de **solo** lectura en el formato siguiente: "*X*.0.0. *YYYY "* donde *X* representa el número de versión principal y *YYYY representa* el número de compilación.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que, al hacer clic en él, muestra un cuadro de mensaje que contiene la información de versión de Reproductor de Windows Media. El **objeto Player** se creó con id. = "Player".


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





