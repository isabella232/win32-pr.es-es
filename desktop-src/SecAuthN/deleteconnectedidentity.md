---
description: Elimina la credencial de usuario utilizada para la identidad conectada.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Función DeleteConnectedIdentity (Indentitystore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 7e59beeb17f7d6d0cced96daaceef7440523c3ce603d759f18cc69a93c0ab05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008473"
---
# <a name="deleteconnectedidentity-function"></a>Función DeleteConnectedIdentity

Elimina la credencial de usuario utilizada para la identidad conectada.

## <a name="syntax"></a>Sintaxis


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProviderHandle* \[ En\]
</dt> <dd>

Identificador del proveedor de identidades.

</dd> <dt>

*UserToken* \[ en, opcional\]
</dt> <dd>

Token del usuario conectado cuya cuenta se va a convertir en una cuenta local. Si *UserToken* no es **NULL,** el proveedor de identidades usa este token para cargar el perfil de usuario y limpiar los estados conectados. Si *UserToken* es **NULL,** LSA fuerza la desconexión. El proveedor de identidades debe limpiar los estados conectados globales en este usuario, pero el proveedor no tiene que limpiar los estados conectados en el perfil de usuario.

</dd> <dt>

*UserSid* \[ En\]
</dt> <dd>

SID principal del usuario conectado. Si *UserToken* no es **NULL,** este parámetro es el SID del usuario del token. Si *UserToken* es **NULL,** este parámetro se usa para identificar al usuario conectado y limpiar los estados conectados globales de ese usuario.

</dd> <dt>

*IdentityUserName* \[ En\]
</dt> <dd>

Nombre de usuario de la identidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, la función puede devolver uno de los siguientes códigos de error.



| Valor devuelto                                                                                               | Descripción                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>PARÁMETRO STATUS \_ INVALID \_</dt> </dl>      | Un parámetro no es válido.<br/>                                                                                                                        |
| <dl> <dt>ESTADO \_ NO \_ TAL \_ USUARIO</dt> </dl>          | El usuario identificado por *UserSid* no existe, no está conectado actualmente o no hay ninguna identidad cuyo nombre de usuario coincida con *IdentityUserName*.<br/> |
| <dl> <dt>RECURSOS \_ INSUFICIENTES \_ DE ESTADO</dt> </dl> | No hay suficiente memoria para procesar la solicitud.<br/>                                                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Indentitystore.h</dt> </dl> |



 

 




