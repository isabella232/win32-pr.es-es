---
title: Función DsRestoreEnd (Ntdsbcli.h)
description: Se llama para finalizar una operación de restauración.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- Función DsRestoreEnd Active Directory
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fbea2559517f6cc541d89817ab32c9d1992da4907f399b94830b41b1b0c1c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191821"
---
# <a name="dsrestoreend-function"></a>Función DsRestoreEnd

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. Use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

Se **llama a la función DsRestoreEnd** para finalizar una operación de restauración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hbc* \[ En\]
</dt> <dd>

Contiene el identificador de contexto de restauración obtenido con la [**función DsRestorePrepare.**](dsrestoreprepare.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran los códigos de error posibles.

<dl> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> <dd>

*hbc* no es válido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **función DsRestoreEnd** cierra los identificadores de enlace pendientes y realiza una operación de limpieza después de un intento de restauración.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[Restaurar un servidor Active Directory servidor](restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

