---
description: Habilita las páginas del lado servidor hospedadas en un asistente para comprobar que el usuario se ha autenticado a través de un cuenta Microsoft.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Método NewWDEvents. PassportAuthenticate (Shldisp. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819043"
---
# <a name="newwdeventspassportauthenticate-method"></a>NewWDEvents. PassportAuthenticate, método

Habilita las páginas del lado servidor hospedadas en un asistente para comprobar que el usuario se ha autenticado a través de un cuenta Microsoft.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrSignInUrl* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Una cadena que contiene la dirección URL de una página web que redirige a la interfaz de usuario del registro de cuenta Microsoft.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **booleano**

Establézcalo en **true** si la autenticación se realiza correctamente; de lo contrario, **false** .

## <a name="remarks"></a>Observaciones

Se puede llamar a este método incluso si un usuario ya ha iniciado sesión en un cuenta Microsoft. En ese caso, el método devuelve **true** sin mostrar el cuenta Microsoft la interfaz de usuario de inicio de sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6,0 o posterior)</dt> </dl> |



 

 
