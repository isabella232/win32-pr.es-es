---
description: Devuelve una estructura NCRYPT SSL CIPHER LENGTHS que contiene las longitudes de encabezado y finalizador del protocolo de entrada, el conjunto de cifrado \_ y el tipo de \_ \_ clave.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Función SslLookupCipherLengths (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 3898b54946b9a1035ce8ec1fedabc218c750bff6579b39f195a1f60b378144f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905996"
---
# <a name="ssllookupcipherlengths-function"></a>Función SslLookupCipherLengths

La **función SslLookupCipherLengths** devuelve una estructura [**NCRYPT SSL CIPHER \_ \_ \_ LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) que contiene las longitudes de encabezado y finalizador del protocolo de entrada, el conjunto de cifrado y el tipo de clave.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
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

*pCipherLengths* \[ out\]
</dt> <dd>

Puntero a un búfer para recibir la estructura [**NCRYPT \_ SSL CIPHER \_ \_ LENGTHS.**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**)

</dd> <dt>

*cbCipherLengths* \[ En\]
</dt> <dd>

Longitud, en bytes, del búfer al que apunta el *parámetro pCipherLengths.*

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro está reservado para uso futuro y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | El *parámetro hSslProvider* contiene un puntero que no es válido.<br/>                                                      |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro pCipherLengths* se establece en **NULL** o la longitud del búfer especificada por *cbCipherLengths* es demasiado corta.<br/> |
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | El *parámetro dwFlags* debe establecerse en cero.<br/>                                                                            |



 

## <a name="remarks"></a>Observaciones

Se llama a la función **SslLookupCipherLengths** para las conversaciones del protocolo de seguridad de la capa de transporte [*(TLS)*](/windows/desktop/SecGloss/t-gly) 1.1 o posterior para consultar las longitudes de encabezado y finalizador del protocolo, conjunto de cifrado y tipo de clave solicitados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

