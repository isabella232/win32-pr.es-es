---
description: Calcula un hash que se usará durante la autenticación del certificado.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Función SslComputeClientAuthHash (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073642"
---
# <a name="sslcomputeclientauthhash-function"></a>Función SslComputeClientAuthHash

La **función SslComputeClientAuthHash** calcula un [*hash*](/windows/desktop/SecGloss/h-gly) que se usará durante la [*autenticación de*](/windows/desktop/SecGloss/c-gly) certificados.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
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

Identificador de la instancia [*del proveedor Capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) protocolo de protocolo de acceso (SSL).

</dd> <dt>

*hMasterKey* \[ En\]
</dt> <dd>

Identificador del objeto [*de clave*](/windows/desktop/SecGloss/m-gly) maestra.

</dd> <dt>

*hHandshakeHash* \[ En\]
</dt> <dd>

Identificador del hash del protocolo de enlace calculado hasta ahora.

</dd> <dt>

*pszAlgId* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que identifica el algoritmo [*criptográfico solicitado.*](/windows/desktop/SecGloss/c-gly) Puede ser uno de los identificadores de algoritmo [**CNG**](cng-algorithm-identifiers.md) estándar o el identificador de otro algoritmo registrado.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Dirección de un búfer que recibe la [*clave BLOB.*](/windows/desktop/SecGloss/k-gly) El *parámetro cbOutput* contiene el tamaño de este búfer. Si este parámetro es **NULL,** esta función colocará el tamaño necesario, en bytes, en el **DWORD** al que apunta el *parámetro byteResult.*

</dd> <dt>

*cbOutput* \[ En\]
</dt> <dd>

Longitud, en bytes, del *búfer pbOutput.*

</dd> <dt>

*pwResult* \[ out\]
</dt> <dd>

Puntero a un **valor DWORD** que especifica la longitud, en bytes, del hash escrito en el *búfer pbOutput.*

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



 

## <a name="remarks"></a>Observaciones

La **función SslComputeClientAuthHash** calcula el hash que se envía en el mensaje de comprobación del certificado del protocolo de enlace SSL. El valor hash se calcula mediante la creación de un hash que contiene el secreto maestro con un hash de todos los mensajes de protocolo de enlace anteriores enviados o recibidos. Para obtener más información sobre la secuencia de protocolo de enlace SSL, vea Descripción del protocolo de enlace [Capa de sockets seguros (SSL).](https://support.microsoft.com/kb/257591)

La manera en que se calcula el hash depende del protocolo y el conjunto de cifrado usados. Además, el hash depende del tipo de clave de autenticación de cliente usada; El *parámetro pszAlgId* indica el tipo de clave que se usa para la autenticación de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

