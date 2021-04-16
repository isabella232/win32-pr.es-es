---
title: External. attemptLogin (método)
description: El método attemptLogin muestra un cuadro de diálogo para que el usuario pueda intentar iniciar sesión en la tienda en línea.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- método attemptLogin de Windows Media Player
- método attemptLogin de Windows Media Player, clase externa
- Clase externa Windows Media Player, método attemptLogin
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699729"
---
# <a name="externalattemptlogin-method"></a>External. attemptLogin (método)

El método **attemptLogin** muestra un cuadro de diálogo para que el usuario pueda intentar iniciar sesión en la tienda en línea.

## <a name="syntax"></a>Sintaxis


```JScript
External.attemptLogin()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el intento de inicio de sesión produce un cambio en el estado de inicio de sesión, Windows Media Player genera el evento [OnLoginChange](external-onloginchange-event.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Evento external. OnLoginChange**](external-onloginchange-event.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner:: login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**Administrar inicio de sesión**](managing-login.md)
</dt> </dl>

 

 





