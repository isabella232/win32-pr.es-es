---
description: Permite que las páginas del lado servidor hospedadas en un asistente comprueben que el usuario se ha autenticado a través de una cuenta Microsoft.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Método NewWDEvents.PassportAuthenticate (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267884"
---
# <a name="newwdeventspassportauthenticate-method"></a>Método NewWDEvents.PassportAuthenticate

Permite que las páginas del lado servidor hospedadas en un asistente comprueben que el usuario se ha autenticado a través de una cuenta Microsoft.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrSignInUrl* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena que contiene la dirección URL de una página web que redirige al inicio de sesión de la cuenta Microsoft en la interfaz de usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **booleano**

Establezca en **true si** la autenticación se realiza correctamente; en caso contrario, **false.**

## <a name="remarks"></a>Observaciones

Se puede llamar a este método incluso si un usuario ya ha iniciado sesión en una cuenta Microsoft. En ese caso, el método devuelve **true sin** mostrar el inicio de sesión de la cuenta Microsoft en la interfaz de usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6.0 o posterior)</dt> </dl> |



 

 
