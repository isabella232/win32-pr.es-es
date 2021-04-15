---
title: Player. launchURL (método)
description: El método launchURL envía una dirección URL al explorador predeterminado del usuario que se va a representar. | Player. launchURL (método)
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- método launchURL de Windows Media Player
- método launchURL Windows Media Player, clase Player
- Clase Player Media Player Windows, método launchURL
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
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690156"
---
# <a name="playerlaunchurl-method"></a>Player. launchURL (método)

El método **launchURL** envía una dirección URL al explorador predeterminado del usuario que se va a representar.

## <a name="syntax"></a>Sintaxis


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dirección URL* \[ de\]
</dt> <dd>

Valor de **cadena** que representa la dirección URL que se va a iniciar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método solo abre páginas web mediante los protocolos HTTP o HTTPS.

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que, cuando se hace clic en él, muestra el sitio web de Microsoft en una nueva ventana del explorador. El elemento **Player** se creó con ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
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

 

 





