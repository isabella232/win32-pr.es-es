---
title: Función DsSetCurrentBackupLog (Ntdsbcli. h)
description: Establece el número de registro de copia de seguridad actual después de una restauración correcta.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsSetCurrentBackupLog
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905372"
---
# <a name="dssetcurrentbackuplog-function"></a>DsSetCurrentBackupLog función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsSetCurrentBackupLog** establece el número de registro de copia de seguridad actual después de una restauración correcta. Dado que Active Directory Domain Services solo admiten el registro circular, esta función no se utiliza normalmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szServerName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre del servidor para el que se va a establecer el número de registro de copia de seguridad. Las barras diagonales inversas anteriores son opcionales. El servidor debe ser el mismo equipo desde el que se llama a esta función. El nombre del servidor no puede contener caracteres de subrayado ( \_ ). Un ejemplo de un nombre de servidor es " \\ \\ server1".

</dd> <dt>

*dwCurrentLog* \[ de\]
</dt> <dd>

Contiene el número de registro de copia de seguridad que se va a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran los posibles códigos de error.

<dl> <dt>

**ERROR \_ de \_ parámetro no válido**
</dt> <dd>

Uno o más parámetros no son válidos.

</dd> <dt>

**ERROR \_ de \_ memoria insuficiente \_**
</dt> <dd>

Error de asignación de memoria.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Normalmente no es necesario llamar a la función **DsSetCurrentBackupLog** . Las funciones de copia de seguridad determinan y establecen automáticamente el último número de registro del que se realizó una copia de seguridad. Use **DsSetCurrentBackupLog** para impedir que otra copia de seguridad incremental se realice correctamente hasta que se realice una copia de seguridad completa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsSetCurrentBackupLogW** (Unicode) y **DsSetCurrentBackupLogA** (ANSI)<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Copia de seguridad y restauración de un servidor Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

