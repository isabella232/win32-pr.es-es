---
description: Calcula el hash enviado en el mensaje finalizado del protocolo de enlace Capa de sockets seguros protocolo de enlace (SSL).
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Función SslComputeFinishedHash (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e0f23a58111bfcebbe668cd3b6c50a135da0dae240907f09a65d60ef1cebdda8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907146"
---
# <a name="sslcomputefinishedhash-function"></a>Función SslComputeFinishedHash

La **función SslComputeFinishedHash** calcula el [*hash*](/windows/desktop/SecGloss/h-gly) enviado en el mensaje finalizado del protocolo de enlace [*Capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) protocolo de enlace (SSL). Para obtener más información sobre la secuencia de protocolo de enlace SSL, vea Descripción del protocolo de enlace [Capa de sockets seguros (SSL).](https://support.microsoft.com/kb/257591)

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo SSL.

</dd> <dt>

*hMasterKey* \[ En\]
</dt> <dd>

Identificador del objeto [*de clave*](/windows/desktop/SecGloss/m-gly) maestra.

</dd> <dt>

*hHandshakeHash* \[ En\]
</dt> <dd>

Identificador del hash de los mensajes de protocolo de enlace.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe el hash para el mensaje de fin.

</dd> <dt>

*cbOutput* \[ En\]
</dt> <dd>

Longitud, en bytes, del *búfer pbOutput.*

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Una de las siguientes constantes.



| Value                                                                                                                                                                                                                                                      | Significado                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ Marca \_ de \_ CLIENTE SSL**</dt> <dt>0x00000001</dt> </dl> | Especifica que se trata de una llamada de cliente.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ MARCA \_ DE \_ SERVIDOR SSL**</dt> <dt>0x00000002</dt> </dl> | Especifica que se trata de una llamada de servidor.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.



| Código o valor devuelto                                                                                                                                                                | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ Identificador \_ no**</dt> <dt>válido 2148073510 (0x80090026)</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

La **función SslComputeFinishedHash** es una de las tres funciones que se usan para generar un hash que se usará durante el protocolo de enlace SSL.

1.  Se llama a la función [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) para obtener un identificador hash.
2.  La [**función SslHashHandshake**](sslhashhandshake.md) se llama varias veces con el identificador hash para agregar datos al hash.
3.  Se **llama a la función SslComputeFinishedHash** con el identificador hash para obtener la síntesis de los datos con hash.

El valor hash se calcula mediante el algoritmo hash del secreto maestro con un hash de todos los mensajes de protocolo de enlace anteriores enviados o recibidos.

El valor de *cbOutput* determina la longitud de los datos hash. Cuando se [*usa el protocolo*](/windows/desktop/SecGloss/t-gly) TLS 1.0 de seguridad de la capa de transporte, siempre debe ser 12 (bytes). Para obtener más información, [vea La versión 1.0](https://www.ietf.org/rfc/rfc2246.txt)del protocolo TLS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

