---
description: Realiza una operación de intercambio de claves Capa de sockets seguros del lado servidor (SSL).
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Función SslImportMasterKey (Sslprovider.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250382"
---
# <a name="sslimportmasterkey-function"></a>Función SslImportMasterKey

La **función SslImportMasterKey** realiza una operación de intercambio de claves [*Capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) del lado servidor (SSL).

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

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo SSL.

</dd> <dt>

*hPrivateKey* \[ En\]
</dt> <dd>

Identificador de la [*clave privada usada*](/windows/desktop/SecGloss/p-gly) en el intercambio.

</dd> <dt>

*phMasterKey* \[ out\]
</dt> <dd>

Puntero al identificador para recibir la [*clave maestra*](/windows/desktop/SecGloss/m-gly).

</dd> <dt>

*dwProtocol* \[ En\]
</dt> <dd>

Uno de los valores [**de Identificador de protocolo de proveedor SSL de CNG.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ En\]
</dt> <dd>

Uno de los valores de Identificadores del conjunto de cifrado [**del proveedor SSL de CNG.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*pParameterList* \[ En\]
</dt> <dd>

Puntero a una matriz de búferes [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contienen información utilizada como parte de la operación de intercambio de claves. El conjunto preciso de búferes depende del protocolo y del conjunto de cifrado que se usa. Como mínimo, la lista contendrá búferes que contienen los valores aleatorios proporcionados por el cliente y el servidor.

</dd> <dt>

*pbEncryptedKey* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene la clave secreta premaster cifrada cifrada con [*la clave pública*](/windows/desktop/SecGloss/p-gly) del servidor.

</dd> <dt>

*cbEncryptedKey* \[ En\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbEncryptedKey.*

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Establezca este parámetro en **NCRYPT \_ SSL SERVER \_ \_ FLAG** para indicar que se trata de una llamada de servidor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | Uno de los identificadores proporcionados no es válido.<br/>                     |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro phMasterKey* es **NULL.**<br/>                      |



 

## <a name="remarks"></a>Observaciones

Esta función descifra el secreto premaster, calcula el secreto maestro SSL y devuelve un identificador a este objeto al autor de la llamada. A continuación, esta clave maestra se puede usar para derivar la clave de sesión SSL y finalizar el protocolo de enlace SSL.

> [!Note]  
> Esta función se usa cuando se usa el algoritmo de intercambio de claves [*RSA.*](/windows/desktop/SecGloss/r-gly) Cuando [*se usa DH,*](/windows/desktop/SecGloss/d-gly) el código de servidor llama a [**SslGenerateMasterKey en**](sslgeneratemasterkey.md) su lugar.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

