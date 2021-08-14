---
description: Comprueba que se ha cargado el perfil de usuario en línea.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Función OnProfileLoaded (Lsaidprov.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 6a8ed0d96ab7c9c63f9574472cac0daedba54e42beec244271efcc309c04dd95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921149"
---
# <a name="onprofileloaded-function"></a>Función OnProfileLoaded

Comprueba que se ha cargado el perfil de usuario en línea.

## <a name="syntax"></a>Sintaxis


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProviderHandle* \[ En\]
</dt> <dd>

Identificador del proveedor.

</dd> <dt>

*UserToken* \[ En\]
</dt> <dd>

Token del usuario cuyo perfil se está cargando o descargando.

</dd> <dt>

*Cargado* \[ En\]
</dt> <dd>

**TRUE** si se ha cargado el perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve STATUS \_ SUCCESS.

Si se produce un error en la función, la función devuelve un código de error distinto de cero que es un error específico del proveedor con fines de diagnóstico.

## <a name="remarks"></a>Comentarios

Se llama a esta función cada vez que se llama a la función [**LoadUserProfile.**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) No se sincroniza con **LoadUserProfile**; Es decir, **LoadUserProfile** podría haber devuelto y el perfil podría haber sido descargado en el momento en que se llamó a la función. Se puede llamar a esta función más de una vez incluso cuando se ha cargado el perfil. El proveedor de identidades no debe suponer que una llamada a esta función con *Loaded* igual a TRUE va a ir seguida de una llamada *con Loaded* igual a FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Lsaidprov.h</dt> </dl> |



 

 
