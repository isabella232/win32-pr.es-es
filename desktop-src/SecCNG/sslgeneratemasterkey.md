---
description: Calcula la clave secreta maestra Capa de sockets seguros protocolo de cifrado (SSL).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Función SslGenerateMasterKey (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4e1ca35493667cb6e7e3d5ba8b162a3d073d51fc397ce2e1a1da7ab7a380728d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906258"
---
# <a name="sslgeneratemasterkey-function"></a>Función SslGenerateMasterKey

La **función SslGenerateMasterKey** calcula la [*clave secreta maestra Capa de sockets seguros protocolo*](/windows/desktop/SecGloss/s-gly) de seguridad (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hPrivateKey* \[ En\]
</dt> <dd>

Identificador de la [*clave privada usada*](/windows/desktop/SecGloss/p-gly) en el intercambio.

</dd> <dt>

*hPublicKey* \[ En\]
</dt> <dd>

Identificador de la [*clave pública usada*](/windows/desktop/SecGloss/p-gly) en el intercambio.

</dd> <dt>

*phMasterKey* \[ out\]
</dt> <dd>

Puntero al identificador de la clave [*maestra generada.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*dwProtocol* \[ En\]
</dt> <dd>

Uno de los valores [**de Identificador de protocolo de proveedor SSL de CNG.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ En\]
</dt> <dd>

Uno de los valores del identificador del conjunto de cifrado del proveedor SSL de [**CNG.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*pParameterList* \[ En\]
</dt> <dd>

Puntero a una matriz de búferes [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contienen información utilizada como parte de la operación de intercambio de claves. El conjunto preciso de búferes depende del protocolo y del conjunto de cifrado que se usa. Como mínimo, la lista contendrá búferes que contienen los valores aleatorios proporcionados por el cliente y el servidor.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Dirección de un búfer que recibe el secreto premaster cifrado con la clave pública del servidor. El *parámetro cbOutput* contiene el tamaño de este búfer. Si este parámetro es **NULL,** esta función devuelve el tamaño necesario, en bytes, en el **DWORD** al que apunta el *parámetro byteResult.*

> [!Note]  
> Este búfer se usa al realizar un intercambio de claves RSA.

 

</dd> <dt>

*cbOutput* \[ En\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbOutput.*

</dd> <dt>

*pwResult* \[ out\]
</dt> <dd>

Puntero a un valor **DWORD** en el que se va a colocar el número de bytes escritos en el *búfer pbOutput.*

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Especifica si esta función se usa para el intercambio de claves del lado cliente o del lado servidor.



| Value                                                                                                                                                                                                                                                      | Significado                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ Marca \_ de \_ cliente SSL**</dt> <dt>0x00000001</dt> </dl> | Especifica un intercambio de claves del lado cliente.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ Marca \_ de \_ servidor SSL**</dt> <dt>0x00000002</dt> </dl> | Especifica un intercambio de claves del lado servidor.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | Uno de los identificadores proporcionados no es válido.<br/>                     |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro phMasterKey* o *hPublicKey* no es válido.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

