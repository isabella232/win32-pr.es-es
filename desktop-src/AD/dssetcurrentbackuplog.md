---
title: Función DsSetCurrentBackupLog (Ntdsbcli.h)
description: Establece el número de registro de copia de seguridad actual después de una restauración correcta.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Función DsSetCurrentBackupLog Active Directory
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
ms.openlocfilehash: ab10ac21d1a3cb2501a809b938252414c756bdfbd62f1e142ba3b902cde8c291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191784"
---
# <a name="dssetcurrentbackuplog-function"></a>Función DsSetCurrentBackupLog

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsSetCurrentBackupLog** establece el número de registro de copia de seguridad actual después de una restauración correcta. Dado Active Directory Domain Services solo admiten el registro circular, esta función no se usa normalmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szServerName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre del servidor para el que se establece el número de registro de copia de seguridad. Las barras diagonales inversas anteriores son opcionales. El servidor debe ser el mismo equipo desde el que se llama a esta función. El nombre del servidor no puede contener caracteres de subrayado ( \_ ). Un ejemplo de un nombre de servidor es \\ \\ "server1".

</dd> <dt>

*dwCurrentLog* \[ En\]
</dt> <dd>

Contiene el número de registro de copia de seguridad que se establecerá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran los códigos de error posibles.

<dl> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> <dd>

Uno o varios parámetros no son válidos.

</dd> <dt>

**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**
</dt> <dd>

Error de asignación de memoria.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Normalmente no es necesario llamar a la función **DsSetCurrentBackupLog.** Las funciones de copia de seguridad determinan y establecen automáticamente el último número de registro del que se ha copiado la copia de seguridad. Use **DsSetCurrentBackupLog para** evitar que otra copia de seguridad incremental se realice correctamente hasta que se realice una copia de seguridad completa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsSetCurrentBackupLogW** (Unicode) y **DsSetCurrentBackupLogA** (ANSI)<br/>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Copia de seguridad y restauración de un servidor Active Directory servidor](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

