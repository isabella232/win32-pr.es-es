---
description: 'Devuelve el identificador del algoritmo Cryptography API: Next Generation (CNG) del algoritmo hash que se usa para la función pseudoaleatorios (PRF) del Protocolo de seguridad de la capa de transporte (TLS) para el protocolo de entrada, el conjunto de cifrado y el tipo de clave.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Función SslGetCipherSuitePRFHashAlgorithm (Sslprovider. h)
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
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669986"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a>SslGetCipherSuitePRFHashAlgorithm función)

La función **SslGetCipherSuitePRFHashAlgorithm** devuelve el identificador del algoritmo Cryptography API: Next Generation (CNG) del [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) que se usa para la [*función pseudoaleatorios*](/windows/desktop/SecGloss/p-gly) (PRF) del Protocolo de seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) para el protocolo de entrada, el conjunto de cifrado y el tipo de clave.

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

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

Uno de los valores del [**identificador de tipo de clave del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . En el caso de los tipos de clave que no son [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC), establezca este parámetro en cero.

</dd> <dt>

*szPRFHash* \[ enuncia\]
</dt> <dd>

Uno de los [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) para el hash que se utilizará para el PRF de TLS.

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
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *szPRFHash* se establece en **null**.<br/>                                     |
| <dl> <dt>**NTE \_ 0x80090029L no \_ compatible**</dt> <dt></dt> </dl>     | La función seleccionada no se admite en la versión especificada de la interfaz.<br/> |
| <dl> <dt>**NTE \_ \_Marcas no válidas**</dt> <dt>0x80090009L</dt> </dl>         | El parámetro *dwFlags* debe establecerse en cero.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

Se llama a esta función **SslGetCipherSuitePRFHashAlgorithm** para las conversaciones TLS 1,2 o posteriores con el fin de consultar el algoritmo hash que se usará en el PRF de TLS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

