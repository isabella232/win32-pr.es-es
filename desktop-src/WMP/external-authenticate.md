---
title: Método External.authenticate
description: El método authenticate inicia un intento de autenticar al usuario.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- authenticate method Reproductor de Windows Media
- authenticate method Reproductor de Windows Media , External (clase)
- Clase externa Reproductor de Windows Media , método de autenticación
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b72c4d20cdd8232746175d966856a616bca9629657ca66c35727b8af8e21178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649555"
---
# <a name="externalauthenticate-method"></a>Método External.authenticate

El **método authenticate** inicia un intento de autenticar al usuario.

## <a name="syntax"></a>Sintaxis


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AuthenticationIndex* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice de una página web de autenticación correcta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Algunos vínculos de una página de detección tienen destinos que solo se deben mostrar una vez autenticado el usuario. La página de detección, Reproductor de Windows Media y el complemento de la tienda en línea usan los pasos siguientes para autenticar al usuario y mostrar la página web de destino:

1.  El script de una página de detección llama a *external*. **método authenticate.**
2.  Reproductor de Windows Media muestra un cuadro de diálogo para obtener un nombre de usuario y una contraseña.
3.  Reproductor de Windows Media llama a [IWMPContentPartner::Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), que inicia el intento de autenticación y devuelve inmediatamente.
4.  Una vez completado el intento de autenticación, el complemento de la tienda en línea llama a [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), pasando wmpcnAuthResult y un valor booleano que indica si el intento se ha realizado correctamente.
5.  Si el intento de autenticación se ha realizado correctamente, Reproductor de Windows Media llama a [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), pasando g \_ szItemInfo AuthenticationSuccessURL, para obtener la dirección URL de una página web de autenticación \_ correcta. En esta llamada, Reproductor de Windows Media pasa el mismo índice que la página de detección pasado a *External*. **método authenticate.**
6.  Reproductor de Windows Media muestra la página web de autenticación correcta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





