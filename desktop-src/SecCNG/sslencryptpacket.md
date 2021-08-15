---
description: Cifra un único paquete Capa de sockets seguros protocolo de seguridad (SSL).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Función SslEncryptPacket (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 74c489cae777b6ca7ac93020fb80ab198622fae97640c09cbd99544c2dafa4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906667"
---
# <a name="sslencryptpacket-function"></a>Función SslEncryptPacket

La **función SslEncryptPacket** cifra un único [*Capa de sockets seguros de protocolo de cifrado*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
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

Identificador de la clave que se usa para cifrar el paquete.

</dd> <dt>

*pbInput* \[ En\]
</dt> <dd>

Puntero al búfer que contiene el paquete que se va a cifrar.

</dd> <dt>

*cbInput* \[ En\]
</dt> <dd>

Longitud, en bytes, del *búfer pbInput.*

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Puntero a un búfer para recibir el paquete cifrado.

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

*dwContentType* \[ En\]
</dt> <dd>

Tipo de contenido que corresponde a este paquete, que especifica el protocolo de nivel superior utilizado para procesar el paquete incluido.



| Value                                                                                                                                                                                                                                           | Significado                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <dt>**CT \_ CAMBIAR \_ LA \_ ESPECIFICACIÓN**</dt> <dt>DE CIFRADO 20</dt> </dl> | Indica un cambio en la estrategia de cifrado.<br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <dt>**CT \_ ALERTA**</dt> <dt>21</dt> </dl>                                          | Indica que el paquete incluido contiene una alerta.<br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <dt>**CT \_ PROTOCOLO DE ENLACE**</dt> <dt>22</dt> </dl>                              | Indica que el paquete incluido forma parte del protocolo de protocolo de enlace.<br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt> </dl>            | Indica que el paquete contiene datos de la aplicación.<br/>                  |



 

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



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

