---
description: Cifra un único paquete de protocolo de Capa de sockets seguros (SSL).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Función SslEncryptPacket (Sslprovider. h)
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
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649291"
---
# <a name="sslencryptpacket-function"></a>SslEncryptPacket función)

La función **SslEncryptPacket** cifra un único paquete de [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hKey* \[ in, out\]
</dt> <dd>

Identificador de la clave que se usa para cifrar el paquete.

</dd> <dt>

*pbInput* \[ de\]
</dt> <dd>

Un puntero al búfer que contiene el paquete que se va a cifrar.

</dd> <dt>

*cbInput* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer *pbInput* .

</dd> <dt>

*pbOutput* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer para recibir el paquete cifrado.

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

*dwContentType* \[ de\]
</dt> <dd>

El tipo de contenido que corresponde a este paquete, que especifica el protocolo de nivel superior que se usa para procesar el paquete delimitado.



| Value                                                                                                                                                                                                                                           | Significado                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <dt>**CT \_ CAMBIAR \_ \_ especificación de cifrado**</dt> <dt>20</dt> </dl> | Indica un cambio en la estrategia de cifrado.<br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <dt>**CT \_ ALERTA**</dt> <dt>21</dt> </dl>                                          | Indica que el paquete incluido contiene una alerta.<br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <dt>**CT \_ Protocolo de enlace**</dt> <dt>22</dt> </dl>                              | Indica que el paquete incluido es parte del Protocolo de enlace.<br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt> </dl>            | Indica que el paquete contiene datos de la aplicación.<br/>                  |



 

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



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

