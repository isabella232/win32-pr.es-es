---
title: External. Authenticate (método)
description: El método Authenticate inicia un intento de autenticación del usuario.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- autenticación de Windows de método Media Player
- método de autenticación de Windows Media Player, clase externa
- Clase externa Windows Media Player, método Authenticate
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
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699728"
---
# <a name="externalauthenticate-method"></a>External. Authenticate (método)

El método **Authenticate** inicia un intento de autenticación del usuario.

## <a name="syntax"></a>Sintaxis


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AuthenticationIndex* \[ de\]
</dt> <dd>

**Número** (**largo**) que especifica el índice de una página web de autenticación correcta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Algunos vínculos de una página de detección tienen destinos que deben mostrarse solo después de que el usuario se haya autenticado. En la página detección, en Windows Media Player y en el complemento de la tienda en línea, siga los pasos que se indican a continuación para autenticar al usuario y mostrar la Página Web de destino:

1.  El script de una página de detección llama a la *externa*. método de **autenticación** .
2.  Windows Media Player muestra un cuadro de diálogo para obtener un nombre de usuario y una contraseña.
3.  Windows Media Player llama a [IWMPContentPartner:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), que inicia el intento de autenticación y vuelve inmediatamente.
4.  Cuando se completa el intento de autenticación, el complemento de la tienda en línea llama a [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), pasando wmpcnAuthResult y un valor booleano que indica si el intento se realizó correctamente.
5.  Si el intento de autenticación se realizó correctamente, Windows Media Player llama a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), pasando g \_ szItemInfo \_ AuthenticationSuccessURL, para obtener la dirección URL de una página web de autenticación correcta. En esta llamada, Windows Media Player pasa el mismo índice que la página de detección pasada a la *externa*. método de **autenticación** .
6.  Windows Media Player muestra la Página Web de autenticación correcta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





