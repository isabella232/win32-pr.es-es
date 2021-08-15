---
description: Enumera los conjuntos de cifrado admitidos por un proveedor Capa de sockets seguros protocolo de cifrado (SSL).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Función SslEnumCipherSuites (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7d9fb40bf6bfebff6d0659640dfb68b718586ac822c8a779a56de300b8d55b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906697"
---
# <a name="sslenumciphersuites-function"></a>Función SslEnumCipherSuites

La **función SslEnumCipherSuites** enumera los conjuntos de cifrado admitidos por un [*proveedor*](/windows/desktop/SecGloss/s-gly) Capa de sockets seguros protocolo de cifrado (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hPrivateKey* \[ in, opcional\]
</dt> <dd>

Identificador de una [*clave privada.*](/windows/desktop/SecGloss/p-gly) Cuando se especifica una clave privada, **SslEnumCipherSuites** enumera los conjuntos de cifrado que son compatibles con la clave privada. Por ejemplo, si la clave privada es una clave DSS, solo se devuelven los conjuntos de cifrado \_ DSS DHE. Si la clave privada es una clave RSA, pero no admite operaciones de descifrado sin procesar, no se devuelven los conjuntos de cifrado SSL2.

Establezca este parámetro en **NULL** cuando no se especifique una clave privada.

> [!Note]  
> Se *obtiene un identificador hPrivateKey* llamando a la función [**SslOpenPrivateKey.**](sslopenprivatekey.md) No se admiten los identificadores obtenidos de la función [**NCryptOpenKey.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey)

 

</dd> <dt>

*ppCipherSuite* \[ out\]
</dt> <dd>

Puntero a una estructura [**NCRYPT \_ SSL CIPHER \_ \_ SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) para recibir la dirección del siguiente conjunto de cifrado de la lista.

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

Puntero a un búfer que indica la posición actual en la lista de conjuntos de cifrado.

Establezca el puntero en **NULL en** la primera llamada a **SslEnumCipherSuites.** En cada llamada posterior, vuelva a pasar el valor sin modificar a **SslEnumCipherSuites.**

Cuando no haya más conjuntos de cifrado disponibles, debe liberar *ppEnumState* llamando a la [**función SslFreeBuffer.**](sslfreebuffer.md)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                    | Descripción                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>      | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/>                     |
| <dl> <dt>**NTE \_ NO \_ MORE \_ ITEMS**</dt> <dt>0x8009002AL</dt> </dl> | No se admiten conjuntos de cifrado adicionales.<br/>                    |



 

## <a name="remarks"></a>Observaciones

Para enumerar todos los conjuntos de cifrado admitidos por el proveedor SSL, llame a la función **SslEnumCipherSuites** en un bucle hasta que **se devuelva NTE \_ NO MORE \_ \_ ITEMS.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Ncrypt.lib</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CONJUNTO DE CIFRADO SSL NCRYPT \_ \_ \_**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

