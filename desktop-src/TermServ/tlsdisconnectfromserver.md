---
title: Función TLSDisconnectFromServer
description: Cierra un identificador abierto a un servidor Escritorio remoto licencias.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- Función TLSDisconnectFromServer Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95911536eda4bd87e45fd034626cf83d88f4d9fc768e4837316ee93abfe3c3d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869415"
---
# <a name="tlsdisconnectfromserver-function"></a>Función TLSDisconnectFromServer

Cierra un identificador abierto a un servidor Escritorio remoto licencias.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hHandle* \[ En\]
</dt> <dd>

Identificador de un Escritorio remoto de licencias que se abre mediante una llamada a la [**función TLSConnectToLsServer.**](tlsconnecttolsserver.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Llame a **la función TLSDisconnectFromServer** como parte de la rutina de limpieza del programa para cerrar todos los identificadores de servidor que abren las llamadas a la [**función TLSConnectToLsServer.**](tlsconnecttolsserver.md)

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

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> </dl>

 

