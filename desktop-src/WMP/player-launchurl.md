---
title: Método Player.launchURL
description: El método launchURL envía una dirección URL al explorador predeterminado del usuario que se va a representar. | Método Player.launchURL
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- Método launchURL Reproductor de Windows Media
- Método launchURL Reproductor de Windows Media , clase Player
- Clase de reproductor Reproductor de Windows Media método , launchURL
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d22c65a29aaee9c849677dfa42acb5769bf30d2fb7079e305ee79632ef22e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134828"
---
# <a name="playerlaunchurl-method"></a>Método Player.launchURL

El **método launchURL** envía una dirección URL al explorador predeterminado del usuario que se va a representar.

## <a name="syntax"></a>Sintaxis


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DIRECCIÓN URL* \[ En\]
</dt> <dd>

**Valor de** cadena que representa la dirección URL que se iniciará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método solo abre páginas web mediante los protocolos HTTP o HTTPS.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que, al hacer clic en él, muestra el sitio web de Microsoft en una nueva ventana del explorador. El **elemento Player** se creó con id. = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
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

 

 





