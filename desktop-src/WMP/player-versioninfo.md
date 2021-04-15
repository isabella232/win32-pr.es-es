---
title: Player. versionInfo
description: La propiedad versionInfo recupera un valor de cadena que especifica la versión de Windows Media Player.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Media Player de Windows Player. versionInfo
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
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708756"
---
# <a name="playerversioninfo"></a>Player. versionInfo

La propiedad **versionInfo** recupera un valor de cadena que especifica la versión de Windows Media Player.

## <a name="syntax"></a>Sintaxis

*reproductor* . **versionInfo**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura con el siguiente formato: "*X*. 0,0. *Yyyy*", donde *X* representa el número de versión principal e *yyyy* representa el número de compilación.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que, cuando se hace clic en él, muestra un cuadro de mensaje que contiene la información de versión de Windows Media Player. El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





