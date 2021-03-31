---
title: Función DsRestoreRegisterComplete (Ntdsbcli. h)
description: Se llama para desbloquear un servidor Active Directory una vez completada una operación de restauración.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsRestoreRegisterComplete
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
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079490"
---
# <a name="dsrestoreregistercomplete-function"></a>DsRestoreRegisterComplete función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Se llama a la función **DsRestoreRegisterComplete** para desbloquear un servidor Active Directory una vez finalizada una operación de restauración. Esta función es equivalente a la función [**DsRestoreRegister**](dsrestoreregister.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HBC* \[ de\]
</dt> <dd>

Contiene el identificador de contexto de restauración obtenido con la función [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*hrRestoreState* \[ de\]
</dt> <dd>

Contiene el estado final de la operación de restauración. Este parámetro debe contener **S \_ OK** si la operación de restauración se realizó correctamente o un código de error en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran los posibles códigos de error.

<dl> <dt>

**ERROR de \_ acceso \_ denegado**
</dt> <dd>

El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función. La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Antes de reiniciar el controlador de dominio, llame a esta función para proporcionar el estado de la operación de restauración. Si el estado no es correcto, el servicio de directorio no se iniciará hasta que se haya restaurado una base de datos válida. Esta función completa la operación de restauración y permite iniciar Active Directory Domain Services.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | No se admite ninguno<br/>                                                               |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Restauración de un servidor de Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

