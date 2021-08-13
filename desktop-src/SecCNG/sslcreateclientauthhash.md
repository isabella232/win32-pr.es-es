---
description: Recupera un identificador para el hash de protocolo de enlace que se usa para la autenticación del cliente.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Función SslCreateClientAuthHash (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 96f1e7fa0de86439f89bf5c4c610bf5b46640533071260852c47321c5a1c6673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907092"
---
# <a name="sslcreateclientauthhash-function"></a>Función SslCreateClientAuthHash

La **función SslCreateClientAuthHash** recupera un identificador para el [*hash*](/windows/desktop/SecGloss/h-gly) de protocolo de enlace que se usa para la autenticación del cliente.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

El identificador de la instancia [*del proveedor Capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) protocolo de seguridad (SSL).

</dd> <dt>

*phHandshakeHash* \[ out\]
</dt> <dd>

Puntero a una variable **HASH \_ HANDLE \_ de NCRYPT** para recibir el identificador hash.

</dd> <dt>

*dwProtocol* \[ En\]
</dt> <dd>

Uno de los valores [**de Identificador de protocolo de proveedor SSL de CNG.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ En\]
</dt> <dd>

Uno de los valores del identificador del conjunto de cifrado del proveedor SSL de [**CNG.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*pszHashAlgId* \[ En\]
</dt> <dd>

Uno de los valores [**de Identificadores de algoritmo CNG.**](cng-algorithm-identifiers.md)

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
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro phHandshakeHash* se establece en **NULL.**<br/>                               |
| <dl> <dt>**NTE \_ NO \_ SE ADMITE**</dt> <dt>0x80090029L</dt> </dl>     | La función seleccionada no se admite en la versión especificada de la interfaz.<br/> |
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insuficiente para asignar búferes.<br/>                                          |
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | El *parámetro dwFlags* debe establecerse en cero.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

Se llama a la función **SslCreateClientAuthHash** para las conversaciones del protocolo de seguridad de la capa de transporte [*(TLS)*](/windows/desktop/SecGloss/t-gly) 1.2 o posterior para crear objetos hash que se usan para aplicar hash a los mensajes de protocolo de enlace. Se llama una vez por cada posible [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) que se puede usar en la firma de autenticación de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

