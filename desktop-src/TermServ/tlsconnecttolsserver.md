---
title: TLSConnectToLsServer función)
description: Abre un identificador del servidor de licencias de Escritorio remoto especificado.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSConnectToLsServer
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
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422416"
---
# <a name="tlsconnecttolsserver-function"></a>TLSConnectToLsServer función)

Abre un identificador del servidor de licencias de Escritorio remoto especificado.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszLsServer* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en **null** que especifica el nombre NetBIOS del servidor de licencias de escritorio remoto. Si el valor de este parámetro es **null**, el servidor especificado es el equipo local.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un identificador del servidor especificado.

Si se produce un error en la función, el valor devuelto es **null**. Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Observaciones

Cuando haya terminado de usar el identificador devuelto por la función **TLSConnectToLsServer** , suéltelo llamando a la función [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**identificador de TLS \_**](tls-handle.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

