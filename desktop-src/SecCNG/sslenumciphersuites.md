---
description: Enumera los conjuntos de cifrado admitidos por un proveedor de protocolo de protocolo Capa de sockets seguros (SSL).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Función SslEnumCipherSuites (Sslprovider. h)
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
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360607"
---
# <a name="sslenumciphersuites-function"></a>SslEnumCipherSuites función)

La función **SslEnumCipherSuites** enumera los conjuntos de cifrado admitidos por un proveedor de protocolo de [*Protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hPrivateKey* \[ en, opcional\]
</dt> <dd>

Identificador de una [*clave privada*](/windows/desktop/SecGloss/p-gly). Cuando se especifica una clave privada, **SslEnumCipherSuites** enumera los conjuntos de cifrado que son compatibles con la clave privada. Por ejemplo, si la clave privada es una clave DSS, solo \_ se devuelven los conjuntos de cifrado de DSS DHE. Si la clave privada es una clave RSA, pero no admite operaciones de descifrado sin procesar, no se devuelven los conjuntos de cifrado de SSL2.

Establezca este parámetro en **null** cuando no especifique una clave privada.

> [!Note]  
> Un identificador *hPrivateKey* se obtiene mediante una llamada a la función [**SslOpenPrivateKey**](sslopenprivatekey.md) . No se admiten los identificadores obtenidos de la función [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) .

 

</dd> <dt>

*ppCipherSuite* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**de \_ \_ \_ conjunto de cifrado SSL de NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) para recibir la dirección del siguiente conjunto de cifrado de la lista.

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

Puntero a un búfer que indica la posición actual en la lista de conjuntos de cifrado.

Establezca el puntero en **null** en la primera llamada a **SslEnumCipherSuites**. En cada llamada subsiguiente, pase el valor sin modificar de nuevo a **SslEnumCipherSuites**.

Cuando no hay más conjuntos de cifrado disponibles, debe liberar *ppEnumState* llamando a la función [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                    | Descripción                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt> </dl>      | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/>                     |
| <dl> <dt>**NTE \_ NO hay \_ más \_ elementos**</dt> <dt>0x8009002AL</dt> </dl> | No se admite ningún conjunto de cifrado adicional.<br/>                    |



 

## <a name="remarks"></a>Observaciones

Para enumerar todos los conjuntos de cifrado admitidos por el proveedor SSL, llame a la función **SslEnumCipherSuites** en un bucle hasta que NTE no se devuelvan **\_ \_ más \_ elementos** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Ncrypt. lib</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_conjunto de \_ cifrado SSL de NCRYPT \_**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

