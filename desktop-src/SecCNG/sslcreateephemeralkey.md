---
description: Crea una clave efímera para su uso durante la autenticación que se produce durante el protocolo de enlace Capa de sockets seguros protocolo de enlace (SSL).
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Función SslCreateEphemeralKey (Sslprovider.h)
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
ms.openlocfilehash: a6a54de2865df805af51b054c22d455d52914a5b00514767d432ceda28c16a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907102"
---
# <a name="sslcreateephemeralkey-function"></a>Función SslCreateEphemeralKey

La **función SslCreateEphemeralKey** crea una clave efímera para su uso durante la autenticación que se produce durante el protocolo de enlace Capa de sockets seguros [*protocolo*](/windows/desktop/SecGloss/s-gly) de enlace (SSL).

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

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*phEphemeralKey* \[ out\]
</dt> <dd>

Identificador de la clave efímera.

</dd> <dt>

*dwProtocol* \[ En\]
</dt> <dd>

Uno de los valores [**de Identificador de protocolo de proveedor SSL de CNG.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ En\]
</dt> <dd>

Uno de los valores del identificador del conjunto de cifrado del proveedor SSL de [**CNG.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwKeyType* \[ En\]
</dt> <dd>

Uno de los valores de Identificador de tipo de clave del proveedor SSL de [**CNG.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) Establezca este parámetro en cero para los tipos de clave que no son criptografía de [*curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC).

</dd> <dt>

*dwKeyBitLen* \[ En\]
</dt> <dd>

Longitud, en bits, de la clave.

</dd> <dt>

*pbParams* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene parámetros para la clave que se va a crear. Si no se usa un conjunto de cifrado de algoritmo de intercambio de claves [*(DHE) Diffie-Hellman (efímero),*](/windows/desktop/SecGloss/d-gly) establezca el parámetro *pbParams* en **NULL** y el *parámetro cbParams* en cero.

</dd> <dt>

*cbParams* \[ En\]
</dt> <dd>

Longitud, en bytes, de los datos del *búfer pbParams.*

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | No hay memoria suficiente para asignar el búfer.<br/> |
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | El *identificador hSslProvider* no es válido.<br/>              |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | Uno de los parámetros proporcionados no es válido.<br/>         |



 

## <a name="remarks"></a>Observaciones

Cuando se usa un conjunto de cifrado DHE, la implementación interna de SSL pasa los parámetros *p* y *g* del servidor a la función **SslCreateEphemeralKey** en los parámetros *pbParams* y *cbParams.*

El formato de los datos del búfer *pbParams* es el mismo que el que se usa al establecer la propiedad [**\_ BCRYPT DH \_ PARAMETERS**](cng-property-identifiers.md) y comienza con una estructura [**\_ BCRYPT DH \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

