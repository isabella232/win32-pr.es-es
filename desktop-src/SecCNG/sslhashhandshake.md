---
description: Devuelve un identificador al hash del protocolo de enlace.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Función SslHashHandshake (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 5a21bdb3fd655e5c3b39249937f04a4122c64e6c6176c0d39ae1164e48863edb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906103"
---
# <a name="sslhashhandshake-function"></a>Función SslHashHandshake

La **función SslHashHandshake** devuelve un identificador al hash del protocolo de enlace.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia [*del proveedor Capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) protocolo de seguridad (SSL).

</dd> <dt>

*hHandshakeHash* \[ in, out\]
</dt> <dd>

Identificador del objeto hash.

</dd> <dt>

*pbInput* \[ out\]
</dt> <dd>

Dirección de un búfer que contiene los datos a los que se va a hash.

</dd> <dt>

*cbInput* \[ En\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbInput.*

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

## <a name="remarks"></a>Observaciones

La **función SslHashHandshake** es una de las tres funciones que se usan para generar un hash que se usará durante el protocolo de enlace SSL.

1.  Se [**llama a la función SslCreateHandshakeHash**](sslcreatehandshakehash.md) para obtener un identificador hash.
2.  Se **llama a la función SslHashHandshake** varias veces con el identificador hash para agregar datos al hash.
3.  Se [**llama a la función SslComputeFinishedHash**](sslcomputefinishedhash.md) con el identificador hash para obtener el resumen de los datos con hash.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

