---
title: Función TLSConnectToLsServer
description: Abre un identificador para el servidor de Escritorio remoto especificado.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- Función TLSConnectToLsServer Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbfc3c1e365a97b8199df34c2e55a8362f48b7f6a2a43e524e3c6e937de5cb0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986975"
---
# <a name="tlsconnecttolsserver-function"></a>Función TLSConnectToLsServer

Abre un identificador para el servidor de Escritorio remoto especificado.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszLsServer* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en **NULL** que especifica el nombre NetBIOS del servidor Escritorio remoto licencias. Si el valor de este parámetro es **NULL,** el servidor especificado es el equipo local.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador para el servidor especificado.

Si se produce un error en la función, el valor devuelto es **NULL.** Para obtener información de error extendida, llame a [**la función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentarios

Cuando haya terminado de usar el identificador devuelto por la función **TLSConnectToLsServer,** suéltelo mediante una llamada a la [**función TLSDisconnectFromServer.**](tlsdisconnectfromserver.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDENTIFICADOR \_ TLS**](tls-handle.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

