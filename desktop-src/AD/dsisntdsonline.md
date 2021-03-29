---
title: Función DsIsNTDSOnline (Ntdsbcli. h)
description: Determina si Active Directory Domain Services están en línea en el servidor especificado.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsIsNTDSOnline
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150325"
---
# <a name="dsisntdsonline-function"></a>DsIsNTDSOnline función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsIsNTDSOnline** determina si Active Directory Domain Services están en línea en el servidor especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szServerName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre del servidor que se va a probar. Las barras diagonales inversas anteriores son opcionales. El servidor debe ser el mismo equipo desde el que se llama a esta función. El nombre del servidor no puede contener caracteres de subrayado ( \_ ). Un ejemplo de un nombre de servidor es " \\ \\ server1".

</dd> <dt>

*pfNTDSOnline* \[ enuncia\]
</dt> <dd>

Puntero al valor **bool** que recibe el resultado. Recibe **true** si el servicio de directorio está en línea o **false** si el servicio de directorio está sin conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK** si la función es correcta o un código de error en caso contrario. En la lista siguiente se enumeran los posibles códigos de error.

<dl> <dt>

**ERROR de \_ acceso \_ denegado**
</dt> <dd>

El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función. La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

No se encuentra el servidor en *szServerName* , no es un controlador de dominio o *szServerName* no tiene el formato correcto. Este valor se define en Ntdsbmsg. h.

</dd> <dt>

**enlace de RPC \_ S \_ no válido \_**
</dt> <dd>

Se está llamando a la función [**DsIsNTDSOnline**](dsisntdsonline.md) de forma remota o el servidor de *szServerName* no es un controlador de dominio.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Llame a esta función antes de llamar a cualquiera de las funciones de copia de seguridad o restauración de directorios. El directorio debe estar en línea para realizar una copia de seguridad. El directorio debe estar sin conexión para realizar una restauración.

Solo se puede llamar a esta función desde un controlador de dominio que también sea el servidor de destino especificado en *szServerName*. No se puede llamar a esta función de forma remota.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsIsNTDSOnlineW** (Unicode) y **DsIsNTDSOnlineA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> <dt>

[Copia de seguridad y restauración de un servidor Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

