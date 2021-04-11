---
description: Calcula un hash que se usará durante la autenticación del certificado.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Función SslComputeClientAuthHash (Sslprovider. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276361"
---
# <a name="sslcomputeclientauthhash-function"></a>SslComputeClientAuthHash función)

La función **SslComputeClientAuthHash** calcula un [*hash*](/windows/desktop/SecGloss/h-gly) que se usará durante la autenticación de [*certificados*](/windows/desktop/SecGloss/c-gly) .

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hMasterKey* \[ de\]
</dt> <dd>

Identificador del objeto de [*clave maestra*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*hHandshakeHash* \[ de\]
</dt> <dd>

Identificador del hash del Protocolo de enlace calculado hasta ahora.

</dd> <dt>

*pszAlgId* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que identifica el [*algoritmo criptográfico*](/windows/desktop/SecGloss/c-gly)solicitado. Puede ser uno de los [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) estándar o el identificador de otro algoritmo registrado.

</dd> <dt>

*pbOutput* \[ enuncia\]
</dt> <dd>

La dirección de un búfer que recibe el [*BLOB de clave*](/windows/desktop/SecGloss/k-gly). El parámetro *cbOutput* contiene el tamaño de este búfer. Si este parámetro es **null**, esta función colocará el tamaño necesario, en bytes, en el **valor DWORD** al que apunta el parámetro *pcbResult* .

</dd> <dt>

*cbOutput* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer *pbOutput* .

</dd> <dt>

*pcbResult* \[ enuncia\]
</dt> <dd>

Un puntero a un valor **DWORD** que especifica la longitud, en bytes, del hash escrito en el búfer de *pbOutput* .

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



 

## <a name="remarks"></a>Observaciones

La función **SslComputeClientAuthHash** calcula el hash que se envía en el mensaje de comprobación de certificado del Protocolo de enlace SSL. El valor hash se calcula creando un hash que contiene el secreto principal con un hash de todos los mensajes de protocolo de enlace anteriores enviados o recibidos. Para obtener más información sobre la secuencia del Protocolo de enlace SSL, vea [Descripción del Protocolo de enlace de capa de sockets seguros (SSL)](https://support.microsoft.com/kb/257591).

La forma en que se calcula el hash depende del protocolo y del conjunto de cifrado utilizado. Además, el hash depende del tipo de clave de autenticación de cliente utilizada. el parámetro *pszAlgId* indica el tipo de clave que se usa para la autenticación del cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

