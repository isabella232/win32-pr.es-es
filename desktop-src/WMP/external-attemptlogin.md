---
title: Método External.attemptLogin
description: El método attemptLogin muestra un cuadro de diálogo para que el usuario pueda intentar iniciar sesión en la tienda en línea.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- Método attemptLogin Reproductor de Windows Media
- método attemptLogin Reproductor de Windows Media , Clase externa
- Clase externa Reproductor de Windows Media método , attemptLogin
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
ms.openlocfilehash: f7f967e812ff76dd11dfd9b4ff07a542d2575548519c3a52816fadf6302a719d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649545"
---
# <a name="externalattemptlogin-method"></a>Método External.attemptLogin

El **método attemptLogin** muestra un cuadro de diálogo para que el usuario pueda intentar iniciar sesión en la tienda en línea.

## <a name="syntax"></a>Sintaxis


```JScript
External.attemptLogin()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si el intento de inicio de sesión produce un cambio en el estado de inicio de sesión, Reproductor de Windows Media el evento [OnLoginChange.](external-onloginchange-event.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Evento External.OnLoginChange**](external-onloginchange-event.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner::Login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**Administración del inicio de sesión**](managing-login.md)
</dt> </dl>

 

 





