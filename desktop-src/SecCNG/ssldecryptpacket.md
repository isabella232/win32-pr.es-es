---
description: Descifra un único Capa de sockets seguros de protocolo de seguridad (SSL).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Función SslDecryptPacket (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 0b058fbb01183ccf0582c0fa196bec71bfaffa2e8a44739c1ea5fb01a8148174
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906707"
---
# <a name="ssldecryptpacket-function"></a>Función SslDecryptPacket

La **función SslDecryptPacket** descifra un único [*Capa de sockets seguros de protocolo de*](/windows/desktop/SecGloss/s-gly) cifrado (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo SSL.

</dd> <dt>

*hKey* \[ in, out\]
</dt> <dd>

Identificador de la clave que se usa para descifrar el paquete.

</dd> <dt>

*pbInput* \[ En\]
</dt> <dd>

Puntero al búfer que contiene el paquete que se va a descifrar.

</dd> <dt>

*cbInput* \[ En\]
</dt> <dd>

Longitud, en bytes, del *búfer pbInput.*

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Puntero a un búfer que contiene el paquete descifrado.

</dd> <dt>

*cbOutput* \[ En\]
</dt> <dd>

Longitud, bytes, del *búfer pbOutput.*

</dd> <dt>

*pwResult* \[ out\]
</dt> <dd>

Número de bytes escritos en el *búfer pbOutput.*

</dd> <dt>

*SequenceNumber* \[ En\]
</dt> <dd>

Número de secuencia que corresponde a este paquete.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                    | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

La longitud del paquete puede ser cero, como cuando se descifra un mensaje "HelloRequest".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

