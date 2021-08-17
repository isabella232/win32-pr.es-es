---
description: Obtiene un identificador hash que se usa para hash de mensajes de protocolo de enlace.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Función SslCreateHandshakeHash (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ea481a5b577c41eafddf9db8d80b4a3a1fe42d801bf96ed8cbc57127a4a8d91e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906832"
---
# <a name="sslcreatehandshakehash-function"></a>Función SslCreateHandshakeHash

La **función SslCreateHandshakeHash** obtiene un identificador hash que se usa para aplicar hash a los mensajes de protocolo de enlace.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia [*del proveedor de protocolos Capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phHandshakeHash* \[ out\]
</dt> <dd>

Identificador hash que se puede pasar a otras funciones del proveedor SSL.

</dd> <dt>

*dwProtocol* \[ En\]
</dt> <dd>

Uno de los valores [**de Identificador de protocolo de proveedor SSL de CNG.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

> [!Note]  
> Esta función no se usa con el protocolo SSL 2.0.

 

</dd> <dt>

*dwCipherSuite* \[ En\]
</dt> <dd>

Uno de los valores de Identificador del conjunto de cifrado del [**proveedor SSL de CNG.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | No hay memoria suficiente para asignar el búfer hash.<br/> |
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | El *identificador hSslProvider* no es válido.<br/>                   |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | *PhHandshakeHash es* null.<br/>                            |



 

## <a name="remarks"></a>Observaciones

La **función SslCreateHandshakeHash** es una de las tres funciones que se usan para generar un hash que se usará durante el protocolo de enlace SSL.

1.  Se llama a la función **SslCreateHandshakeHash** para obtener un identificador hash.
2.  La [**función SslHashHandshake**](sslhashhandshake.md) se llama varias veces con el identificador hash para agregar datos al hash.
3.  Se [**llama a la función SslComputeFinishedHash**](sslcomputefinishedhash.md) con el identificador hash para obtener la síntesis de los datos con hash.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

