---
description: 'Devuelve cryptography API: identificador de algoritmo de próxima generación (CNG) del algoritmo hash que se usa para la función pseudo aleatoria (PRF) del protocolo de seguridad de la capa de transporte (TLS) para el protocolo de entrada, el conjunto de cifrado y el tipo de clave.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Función SslGetCipherSuitePRFHashAlgorithm (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: f328f5e4746d3a66f614e8ccbbfe66bbf3475b7f7a1a98a8a68c11df96412bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906167"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a>Función SslGetCipherSuitePRFHashAlgorithm

La función **SslGetCipherSuitePRFHashAlgorithm** devuelve cryptography API: identificador de algoritmo de próxima generación (CNG) del [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) que se usa para la [*función pseudo*](/windows/desktop/SecGloss/p-gly) aleatoria (PRF) del protocolo de seguridad de la capa de transporte (TLS) para el protocolo de entrada, el conjunto de cifrado y el tipo de clave. [](/windows/desktop/SecGloss/t-gly)

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

El identificador de la instancia [*del proveedor Capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) protocolo de seguridad (SSL).

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

Uno de los valores de Identificador de tipo de clave del proveedor SSL de [**CNG.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) Para los tipos de clave que no [*son criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC), establezca este parámetro en cero.

</dd> <dt>

*szPRFHash* \[ out\]
</dt> <dd>

Uno de los [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) para el hash que se usará para la PRF de TLS.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro está reservado para uso futuro y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | El *parámetro hSslProvider* contiene un puntero que no es válido.<br/>                |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro szPRFHash* se establece en **NULL.**<br/>                                     |
| <dl> <dt>**NTE \_ NO \_ SE ADMITE**</dt> <dt>0x80090029L</dt> </dl>     | La función seleccionada no se admite en la versión especificada de la interfaz.<br/> |
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | El *parámetro dwFlags* debe establecerse en cero.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

Se llama a esta función **SslGetCipherSuitePRFHashAlgorithm** para que las conversaciones de TLS 1.2 o posterior consulten el algoritmo hash que se usará en la PRF de TLS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

