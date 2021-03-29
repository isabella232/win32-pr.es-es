---
description: Comprueba que se ha cargado el perfil de usuario en línea.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Función OnProfileLoaded (Lsaidprov. h)
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
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813603"
---
# <a name="onprofileloaded-function"></a>OnProfileLoaded función)

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

*ProviderHandle* \[ de\]
</dt> <dd>

Identificador del proveedor.

</dd> <dt>

*UserToken* \[ de\]
</dt> <dd>

Token del usuario cuyo perfil se carga o descarga.

</dd> <dt>

*Cargado* \[ de\]
</dt> <dd>

**True** si se ha cargado el perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve el estado \_ Success.

Si se produce un error en la función, la función devuelve un código de error distinto de cero que es un error específico del proveedor con fines de diagnóstico.

## <a name="remarks"></a>Observaciones

Se llama a esta función cada vez que se llama a la función [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) . No está sincronizado con **LoadUserProfile**; es decir, **LoadUserProfile** podría haber devuelto y es posible que se haya descargado el perfil en el momento en que se llamó a la función. Esta función se puede llamar más de una vez incluso cuando se ha cargado el perfil. El proveedor de identidades no debe suponer que una llamada a esta función con la *carga* igual a true irá seguida de una llamada con el valor de *cargado* igual a false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Lsaidprov. h</dt> </dl> |



 

 
