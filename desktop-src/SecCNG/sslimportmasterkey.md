---
description: Realiza una operación de intercambio de claves del Protocolo de Capa de sockets seguros de servidor (SSL).
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Función SslImportMasterKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648382"
---
# <a name="sslimportmasterkey-function"></a>SslImportMasterKey función)

La función **SslImportMasterKey** realiza una operación de intercambio de claves del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) de servidor (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
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

*phMasterKey* \[ enuncia\]
</dt> <dd>

Puntero al identificador para recibir la [*clave maestra*](/windows/desktop/SecGloss/m-gly).

</dd> <dt>

*dwProtocol* \[ de\]
</dt> <dd>

Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ de\]
</dt> <dd>

Uno de los valores de los [**identificadores del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pParameterList* \[ de\]
</dt> <dd>

Puntero a una matriz de búferes de [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contienen información utilizada como parte de la operación de intercambio de claves. El conjunto preciso de búferes depende del protocolo y el conjunto de cifrado que se utiliza. Como mínimo, la lista contendrá búferes que contengan los valores aleatorios proporcionados por el cliente y el servidor.

</dd> <dt>

*pbEncryptedKey* \[ de\]
</dt> <dd>

Un puntero a un búfer que contiene la clave secreta maestra precifrada cifrada con la [*clave pública*](/windows/desktop/SecGloss/p-gly) del servidor.

</dd> <dt>

*cbEncryptedKey* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbEncryptedKey* .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Establezca este parámetro en **la \_ \_ \_ marca de servidor SSL NCRYPT** para indicar que se trata de una llamada de servidor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | Uno de los identificadores proporcionados no es válido.<br/>                     |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *phMasterKey* es **null**.<br/>                      |



 

## <a name="remarks"></a>Observaciones

Esta función descifra el secreto principal previo, calcula el secreto principal SSL y devuelve un identificador de este objeto al llamador. Esta clave maestra se puede usar para derivar la clave de sesión SSL y finalizar el protocolo de enlace SSL.

> [!Note]  
> Esta función se usa cuando se utiliza el algoritmo de intercambio de claves [*RSA*](/windows/desktop/SecGloss/r-gly) . Cuando se usa [*DH*](/windows/desktop/SecGloss/d-gly) , el código de servidor llama a [**SslGenerateMasterKey**](sslgeneratemasterkey.md) en su lugar.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

