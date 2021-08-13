---
description: Devuelve una clave Capa de sockets seguros sesión de protocolo de inicio de sesión (SSL) o una clave efímera pública en un BLOB serializado.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Función SslExportKey (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 073e922ce8c1a79e81d991c869743148b5a581503192a10dfb9cd6e64707d83e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906677"
---
# <a name="sslexportkey-function"></a>Función SslExportKey

La **función SslExportKey** devuelve una clave Capa de sockets seguros de sesión [*de*](/windows/desktop/SecGloss/s-gly) protocolo de Capa de sockets seguros (SSL) [](/windows/desktop/SecGloss/s-gly) o una clave efímera pública en un BLOB [*serializado.*](/windows/desktop/SecGloss/b-gly)

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hKey* \[ En\]
</dt> <dd>

Identificador de la clave que se exportará.

Si no especifica una clave, establezca este parámetro en **NULL.**

> [!Note]  
> Se *obtiene un identificador hKey* llamando a la función [**SslOpenPrivateKey.**](sslopenprivatekey.md) No se admiten los identificadores obtenidos de la función [**NCryptOpenKey.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey)

 

</dd> <dt>

*pszBlobType* \[ En\]
</dt> <dd>

Cadena Unicode terminada en NULL que contiene un identificador que especifica el tipo de BLOB que se exportará. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**BCRYPT \_ DH \_ PUBLIC \_ BLOB**</dt> </dl>    | Exporte una Diffie-Hellman [*pública*](/windows/desktop/SecGloss/p-gly). El *búfer pbOutput* recibe una estructura [**\_ BCRYPT DH KEY \_ \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) seguida inmediatamente de los datos clave.<br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**BCRYPT \_ ECCPUBLIC \_ BLOB**</dt> </dl>     | Exportar una [*clave pública de criptografía*](/windows/desktop/SecGloss/e-gly) de curva elíptica (ECC). El *búfer pbOutput* recibe una estructura [**\_ BCRYPT ECCKEY \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) seguida inmediatamente de los datos clave.<br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**BCRYPT \_ OPAQUE \_ KEY \_ BLOB**</dt> </dl> | Exportar una clave simétrica en un formato específico de un único proveedor [*de servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP). Los blobs opacos no son transferibles  y deben importarse mediante el mismo proveedor de servicios criptográficos (CSP) que generó el BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**BCRYPT \_ RSAPUBLIC \_ BLOB**</dt> </dl>     | Exportar una clave pública RSA. El *búfer pbOutput* recibe una [**estructura \_ BCRYPT RSAKEY \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) inmediatamente seguida de los datos clave.<br/>                                                                                                                                                                                                |



 

</dd> <dt>

*pbOutput* \[ out, opcional\]
</dt> <dd>

Dirección de un búfer que recibe la [*clave BLOB*](/windows/desktop/SecGloss/k-gly). El *parámetro cbOutput* contiene el tamaño de este búfer. Si este parámetro es **NULL,** esta función colocará el tamaño necesario, en bytes, en el **DWORD** al que apunta el *parámetro byteResult.*

</dd> <dt>

*cbOutput* \[ En\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbOutput.*

</dd> <dt>

*pwResult* \[ out\]
</dt> <dd>

Dirección de una variable **DWORD** que recibe el número de bytes copiados en el *búfer pbOutput.* Si el *parámetro pbOutput* se establece en **NULL** cuando se llama a la función, el tamaño necesario para el búfer *pbOutput,* en bytes, se devuelve en el **DWORD** al que apunta este parámetro.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                    | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

La **función SslExportKey** facilita el transporte de claves de sesión de un proceso a otro, así como la exportación de la parte pública de una clave efímera.

Al exportar claves de sesión, el tipo BLOB es opaco, lo que significa que el formato del BLOB es irrelevante siempre que las funciones **SslExportKey** y [**SslImportKey**](sslimportkey.md) puedan interpretarlo.

Al exportar la parte pública de una clave efímera, el tipo BLOB debe ser el tipo adecuado, como **NCRYPT \_ DH PUBLIC \_ \_ BLOB** o **NCRYPT \_ ECCPUBLIC \_ BLOB.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

