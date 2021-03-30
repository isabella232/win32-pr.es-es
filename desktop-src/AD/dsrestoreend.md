---
title: Función DsRestoreEnd (Ntdsbcli. h)
description: Se llama para finalizar una operación de restauración.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsRestoreEnd
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
ms.openlocfilehash: caabbe216875c2fe934f3c87e32688cd17bc8992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079279"
---
# <a name="dsrestoreend-function"></a>DsRestoreEnd función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Se llama a la función **DsRestoreEnd** para finalizar una operación de restauración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HBC* \[ de\]
</dt> <dd>

Contiene el identificador de contexto de restauración obtenido con la función [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran los posibles códigos de error.

<dl> <dt>

**ERROR \_ de \_ parámetro no válido**
</dt> <dd>

*HBC* no es válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función **DsRestoreEnd** cierra los identificadores de enlace pendientes y realiza una operación de limpieza después de un intento de restauración.

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

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[Restauración de un servidor de Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

