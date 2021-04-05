---
description: Descifra un único paquete de protocolo de Capa de sockets seguros (SSL).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Función SslDecryptPacket (Sslprovider. h)
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
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001643"
---
# <a name="ssldecryptpacket-function"></a>SslDecryptPacket función)

la función **SslDecryptPacket** descifra un único paquete de [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hKey* \[ in, out\]
</dt> <dd>

Identificador de la clave que se usa para descifrar el paquete.

</dd> <dt>

*pbInput* \[ de\]
</dt> <dd>

Un puntero al búfer que contiene el paquete que se va a descifrar.

</dd> <dt>

*cbInput* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer *pbInput* .

</dd> <dt>

*pbOutput* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer para que contenga el paquete descifrado.

</dd> <dt>

*cbOutput* \[ de\]
</dt> <dd>

La longitud, bytes, del búfer *pbOutput* .

</dd> <dt>

*pcbResult* \[ enuncia\]
</dt> <dd>

Número de bytes escritos en el búfer de *pbOutput* .

</dd> <dt>

*SequenceNumber* \[ de\]
</dt> <dd>

El número de secuencia que corresponde a este paquete.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                    | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

La longitud del paquete puede ser cero, por ejemplo, cuando se descifra un mensaje "HelloRequest".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

