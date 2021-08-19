---
title: Función DsRestoreRegisterComplete (Ntdsbcli.h)
description: Se llama para desbloquear un servidor Active Directory una vez completada una operación de restauración.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Función DsRestoreRegisterComplete Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b335f67ed4d392d189553f66655797e03121cbdee6ce19dffbd9803199f6c72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429933"
---
# <a name="dsrestoreregistercomplete-function"></a>Función DsRestoreRegisterComplete

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. Use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

Se **llama a la función DsRestoreRegisterComplete** para desbloquear un servidor Active Directory una vez completada una operación de restauración. Esta función es equivalente a la [**función DsRestoreRegister.**](dsrestoreregister.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hbc* \[ En\]
</dt> <dd>

Contiene el identificador de contexto de restauración obtenido con la [**función DsRestorePrepare.**](dsrestoreprepare.md)

</dd> <dt>

*hrRestoreState* \[ En\]
</dt> <dd>

Contiene el estado final de la operación de restauración. Este parámetro debe contener **S \_ OK si** la operación de restauración se ha realizado correctamente o un código de error en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** la función se realiza correctamente o un código de error win32 o RPC en caso contrario. En la lista siguiente se enumeran los posibles códigos de error.

<dl> <dt>

**ACCESO DE ERROR \_ \_ DENEGADO**
</dt> <dd>

El autor de la llamada no tiene los privilegios de acceso adecuados para llamar a esta función. La [**función DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Antes de reiniciar el controlador de dominio, llame a esta función para proporcionar el estado de la operación de restauración. Si el estado no es correcto, el servicio de directorio no se iniciará hasta que se restaure una base de datos válida. Esta función completa la operación de restauración y Active Directory Domain Services iniciar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | No se admite ninguno<br/>                                                               |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Restaurar un servidor Active Directory servidor](restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

