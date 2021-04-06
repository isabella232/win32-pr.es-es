---
description: Devuelve una \_ \_ \_ estructura de longitud de cifrado SSL de NCRYPT que contiene las longitudes de encabezado y finalizador del Protocolo de entrada, el conjunto de cifrado y el tipo de clave.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Función SslLookupCipherLengths (Sslprovider. h)
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
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001595"
---
# <a name="ssllookupcipherlengths-function"></a>SslLookupCipherLengths función)

La función **SslLookupCipherLengths** devuelve una estructura de [**\_ \_ \_ longitudes de cifrado SSL de NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) que contiene las longitudes de encabezado y finalizador del Protocolo de entrada, el conjunto de cifrado y el tipo de clave.

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

*pCipherLengths* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer para recibir la estructura de [**\_ \_ \_ longitudes de cifrado SSL de NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) .

</dd> <dt>

*cbCipherLengths* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer al que apunta el parámetro *pCipherLengths* .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | El parámetro *hSslProvider* contiene un puntero que no es válido.<br/>                                                      |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *pCipherLengths* está establecido en **null** o la longitud del búfer especificada por *cbCipherLengths* es demasiado corta.<br/> |
| <dl> <dt>**NTE \_ \_Marcas no válidas**</dt> <dt>0x80090009L</dt> </dl>         | El parámetro *dwFlags* debe establecerse en cero.<br/>                                                                            |



 

## <a name="remarks"></a>Observaciones

Se llama a la función **SslLookupCipherLengths** para las conversaciones del Protocolo de seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) 1,1 o posteriores para consultar las longitudes de encabezado y finalizador del Protocolo, conjunto de cifrado y tipo de clave solicitados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

