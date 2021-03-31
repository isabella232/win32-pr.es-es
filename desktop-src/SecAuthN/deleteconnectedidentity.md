---
description: Elimina la credencial de usuario usada para la identidad conectada.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Función DeleteConnectedIdentity (Indentitystore. h)
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
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082000"
---
# <a name="deleteconnectedidentity-function"></a>DeleteConnectedIdentity función)

Elimina la credencial de usuario usada para la identidad conectada.

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

*ProviderHandle* \[ de\]
</dt> <dd>

Identificador del proveedor de identidades.

</dd> <dt>

*UserToken* \[ en, opcional\]
</dt> <dd>

Token del usuario conectado cuya cuenta se va a convertir en una cuenta local. Si *UserToken* no es **null**, el proveedor de identidades usa este token para cargar el perfil de usuario y limpiar los Estados conectados. Si *UserToken* es **null**, LSA está forzando la desconexión. El proveedor de identidades debe limpiar todos los Estados conectados globales de este usuario, pero el proveedor no tiene que limpiar los Estados conectados en el perfil de usuario.

</dd> <dt>

*UserSid* \[ de\]
</dt> <dd>

SID principal del usuario conectado. Si *UserToken* no es **null**, este parámetro es el SID de usuario del token. Si *UserToken* es **null**, este parámetro se utiliza para identificar al usuario conectado y limpiar los Estados conectados globales de dicho usuario.

</dd> <dt>

*IdentityUserName* \[ de\]
</dt> <dd>

El nombre de usuario de la identidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, la función puede devolver uno de los siguientes códigos de error.



| Valor devuelto                                                                                               | Descripción                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>ESTADO \_ parámetro no válido \_</dt> </dl>      | Un parámetro no es válido.<br/>                                                                                                                        |
| <dl> <dt>ESTADO \_ no \_ tal \_ usuario</dt> </dl>          | El usuario identificado por *UserSid* no existe, no está conectado actualmente o no hay ninguna identidad cuyo nombre de usuario coincida con *IdentityUserName*.<br/> |
| <dl> <dt>Estado de \_ recursos insuficientes \_</dt> </dl> | No hay suficiente memoria para procesar la solicitud.<br/>                                                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Indentitystore. h</dt> </dl> |



 

 




