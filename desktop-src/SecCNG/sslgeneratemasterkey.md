---
description: Calcula la clave secreta maestra del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Función SslGenerateMasterKey (Sslprovider. h)
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
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424075"
---
# <a name="sslgeneratemasterkey-function"></a>SslGenerateMasterKey función)

La función **SslGenerateMasterKey** calcula la clave secreta maestra del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hPrivateKey* \[ de\]
</dt> <dd>

Identificador de la [*clave privada*](/windows/desktop/SecGloss/p-gly) utilizada en el intercambio.

</dd> <dt>

*hPublicKey* \[ de\]
</dt> <dd>

Identificador de la [*clave pública*](/windows/desktop/SecGloss/p-gly) que se usa en el intercambio.

</dd> <dt>

*phMasterKey* \[ enuncia\]
</dt> <dd>

Puntero al identificador de la [*clave maestra*](/windows/desktop/SecGloss/m-gly)generada.

</dd> <dt>

*dwProtocol* \[ de\]
</dt> <dd>

Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ de\]
</dt> <dd>

Uno de los valores del [**identificador del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pParameterList* \[ de\]
</dt> <dd>

Puntero a una matriz de búferes de [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contienen información utilizada como parte de la operación de intercambio de claves. El conjunto preciso de búferes depende del protocolo y el conjunto de cifrado que se utiliza. Como mínimo, la lista contendrá búferes que contengan los valores aleatorios proporcionados por el cliente y el servidor.

</dd> <dt>

*pbOutput* \[ enuncia\]
</dt> <dd>

Dirección de un búfer que recibe el secreto principal precifrado cifrado con la clave pública del servidor. El parámetro *cbOutput* contiene el tamaño de este búfer. Si este parámetro es **null**, esta función devuelve el tamaño necesario, en bytes, en el **valor DWORD** al que apunta el parámetro *pcbResult* .

> [!Note]  
> Este búfer se usa al realizar un intercambio de claves RSA.

 

</dd> <dt>

*cbOutput* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbOutput* .

</dd> <dt>

*pcbResult* \[ enuncia\]
</dt> <dd>

Un puntero a un valor **DWORD** en el que se colocará el número de bytes escritos en el búfer *pbOutput* .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Especifica si esta función se usa para el intercambio de claves del lado cliente o el servidor.



| Value                                                                                                                                                                                                                                                      | Significado                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Marca de cliente SSL**</dt> <dt>0x00000001</dt> </dl> | Especifica un intercambio de claves del lado cliente.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Marca de servidor SSL**</dt> <dt>0x00000002</dt> </dl> | Especifica un intercambio de claves del lado servidor.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | Uno de los identificadores proporcionados no es válido.<br/>                     |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *phMasterKey* o *hPublicKey* no es válido.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

