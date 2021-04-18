---
description: Recupera un identificador para el hash del Protocolo de enlace que se utiliza para la autenticación del cliente.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Función SslCreateClientAuthHash (Sslprovider. h)
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
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666960"
---
# <a name="sslcreateclientauthhash-function"></a>SslCreateClientAuthHash función)

La función **SslCreateClientAuthHash** recupera un identificador para el [*hash*](/windows/desktop/SecGloss/h-gly) de protocolo de enlace que se usa para la autenticación del cliente.

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phHandshakeHash* \[ enuncia\]
</dt> <dd>

Puntero a una variable **de \_ \_ identificador hash de NCRYPT** para recibir el identificador hash.

</dd> <dt>

*dwProtocol* \[ de\]
</dt> <dd>

Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ de\]
</dt> <dd>

Uno de los valores del [**identificador del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pszHashAlgId* \[ de\]
</dt> <dd>

Uno de los valores de los [**identificadores del algoritmo CNG**](cng-algorithm-identifiers.md) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | El parámetro *hSslProvider* contiene un puntero que no es válido.<br/>                |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *phHandshakeHash* se establece en **null**.<br/>                               |
| <dl> <dt>**NTE \_ 0x80090029L no \_ compatible**</dt> <dt></dt> </dl>     | La función seleccionada no se admite en la versión especificada de la interfaz.<br/> |
| <dl> <dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insuficiente para asignar búferes.<br/>                                          |
| <dl> <dt>**NTE \_ \_Marcas no válidas**</dt> <dt>0x80090009L</dt> </dl>         | El parámetro *dwFlags* debe establecerse en cero.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

Se llama a la función **SslCreateClientAuthHash** para las conversaciones del Protocolo de seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) 1,2 o una versión posterior para crear objetos hash que se utilizan para los mensajes de protocolo de enlace hash. Se llama una vez para cada [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) posible que se puede usar en la firma de autenticación del cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

