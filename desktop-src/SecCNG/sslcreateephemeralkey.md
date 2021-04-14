---
description: Crea una clave efímera para su uso durante la autenticación que se produce durante el protocolo de enlace del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Función SslCreateEphemeralKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648317"
---
# <a name="sslcreateephemeralkey-function"></a>SslCreateEphemeralKey función)

La función **SslCreateEphemeralKey** crea una clave efímera para su uso durante la autenticación que se produce durante el protocolo de enlace del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*phEphemeralKey* \[ enuncia\]
</dt> <dd>

Identificador de la clave efímera.

</dd> <dt>

*dwProtocol* \[ de\]
</dt> <dd>

Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ de\]
</dt> <dd>

Uno de los valores del [**identificador del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwKeyType* \[ de\]
</dt> <dd>

Uno de los valores del [**identificador de tipo de clave del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . Establezca este parámetro en cero para los tipos de clave que no son [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC).

</dd> <dt>

*dwKeyBitLen* \[ de\]
</dt> <dd>

Longitud, en bits, de la clave.

</dd> <dt>

*pbParams* \[ de\]
</dt> <dd>

Un puntero a un búfer para contener los parámetros de la clave que se va a crear. Si no se utiliza un conjunto de cifrado del [*algoritmo de intercambio de claves (DHE) de Diffie-Hellman (efímero)*](/windows/desktop/SecGloss/d-gly) , establezca el parámetro *pbParams* en **null** y el parámetro *cbParams* en cero.

</dd> <dt>

*cbParams* \[ de\]
</dt> <dd>

La longitud, en bytes, de los datos en el búfer de *pbParams* .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt> </dl>         | No hay memoria suficiente para asignar el búfer.<br/> |
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | El identificador de *hSslProvider* no es válido.<br/>              |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | Uno de los parámetros proporcionados no es válido.<br/>         |



 

## <a name="remarks"></a>Observaciones

Cuando se usa un conjunto de cifrado de DHE, la implementación de SSL interna pasa los parámetros de servidor *p* y *g* a la función **SslCreateEphemeralKey** en los parámetros *pbParams* y *cbParams* .

El formato de los datos en el búfer *pbParams* es el mismo que el que se usa al establecer la propiedad [**bcrypt \_ DH \_ Parameters**](cng-property-identifiers.md) , y se inicia con una estructura de [**\_ \_ \_ encabezado de parámetro DH de bcrypt**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

