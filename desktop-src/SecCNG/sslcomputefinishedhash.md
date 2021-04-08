---
description: Calcula el hash enviado en el mensaje finalizado del Protocolo de enlace del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Función SslComputeFinishedHash (Sslprovider. h)
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
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001647"
---
# <a name="sslcomputefinishedhash-function"></a>SslComputeFinishedHash función)

La función **SslComputeFinishedHash** calcula el [*hash*](/windows/desktop/SecGloss/h-gly) enviado en el mensaje finalizado del Protocolo de enlace del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL). Para obtener más información sobre la secuencia del Protocolo de enlace SSL, vea [Descripción del Protocolo de enlace de capa de sockets seguros (SSL)](https://support.microsoft.com/kb/257591).

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hMasterKey* \[ de\]
</dt> <dd>

Identificador del objeto de [*clave maestra*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*hHandshakeHash* \[ de\]
</dt> <dd>

Identificador del hash de los mensajes de protocolo de enlace.

</dd> <dt>

*pbOutput* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe el hash para el mensaje de finalización.

</dd> <dt>

*cbOutput* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer *pbOutput* .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Una de las constantes siguientes.



| Value                                                                                                                                                                                                                                                      | Significado                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Marca de cliente SSL**</dt> <dt>0x00000001</dt> </dl> | Especifica que se trata de una llamada de cliente.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Marca de servidor SSL**</dt> <dt>0x00000002</dt> </dl> | Especifica que se trata de una llamada de servidor.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.



| Código o valor devuelto                                                                                                                                                                | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>2148073510 (0x80090026)</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

La función **SslComputeFinishedHash** es una de las tres funciones que se usan para generar un hash que se usará durante el protocolo de enlace SSL.

1.  Se llama a la función [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) para obtener un identificador hash.
2.  A la función [**SslHashHandshake**](sslhashhandshake.md) se le llama cualquier número de veces con el identificador hash para agregar datos al hash.
3.  Se llama a la función **SslComputeFinishedHash** con el identificador hash para obtener el Resumen de los datos con hash.

El valor hash se calcula mediante el hash del secreto principal con un hash de todos los mensajes de protocolo de enlace anteriores enviados o recibidos.

El valor de *cbOutput* determina la longitud de los datos hash. Cuando se usa el protocolo de seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) 1,0, siempre debe ser 12 (bytes). Para obtener más información, consulte [la versión 1,0 del protocolo TLS](https://www.ietf.org/rfc/rfc2246.txt).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

