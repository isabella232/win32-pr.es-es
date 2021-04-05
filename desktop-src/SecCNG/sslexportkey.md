---
description: Devuelve una clave de sesión de protocolo Capa de sockets seguros (SSL) o una clave efímera pública en un BLOB serializado.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Función SslExportKey (Sslprovider. h)
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
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001642"
---
# <a name="sslexportkey-function"></a>SslExportKey función)

La función **SslExportKey** devuelve una [*clave de sesión*](/windows/desktop/SecGloss/s-gly) de [*Protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL) o una clave efímera pública en un [*BLOB*](/windows/desktop/SecGloss/b-gly)serializado.

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hKey* \[ de\]
</dt> <dd>

Identificador de la clave que se va a exportar.

Si no especifica una clave, establezca este parámetro en **null**.

> [!Note]  
> Un identificador *hKey* se obtiene mediante una llamada a la función [**SslOpenPrivateKey**](sslopenprivatekey.md) . No se admiten los identificadores obtenidos de la función [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) .

 

</dd> <dt>

*pszBlobType* \[ de\]
</dt> <dd>

Una cadena Unicode terminada en null que contiene un identificador que especifica el tipo de BLOB que se va a exportar. Puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**\_ \_ BLOB público de BCRYPT DH \_**</dt> </dl>    | Exportar una [*clave pública*](/windows/desktop/SecGloss/p-gly)de Diffie-Hellman. El búfer *pbOutput* recibe una estructura de BLOB de [**clave de BCRYPT \_ \_ \_ DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) seguida inmediatamente de los datos de clave.<br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**\_BLOB ECCPUBLIC de BCRYPT \_**</dt> </dl>     | Exportar una clave pública de [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC). El búfer *pbOutput* recibe una estructura de [**\_ \_ blobs ECCKEY de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) seguida inmediatamente de los datos clave.<br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**\_BLOB de \_ clave \_ opaca de BCRYPT**</dt> </dl> | Exportar una clave simétrica en un formato específico de un único proveedor de [*servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP). Los blobs opacos no se pueden transferir y se deben importar mediante el mismo *proveedor de servicios criptográficos* (CSP) que generó el BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**\_BLOB RSAPUBLIC de BCRYPT \_**</dt> </dl>     | Exportar una clave pública RSA. El búfer *pbOutput* recibe una estructura de [**\_ \_ blobs RSAKEY de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) seguida inmediatamente de los datos clave.<br/>                                                                                                                                                                                                |



 

</dd> <dt>

*pbOutput* \[ out, opcional\]
</dt> <dd>

La dirección de un búfer que recibe el [*BLOB de clave*](/windows/desktop/SecGloss/k-gly). El parámetro *cbOutput* contiene el tamaño de este búfer. Si este parámetro es **null**, esta función colocará el tamaño necesario, en bytes, en el **valor DWORD** al que apunta el parámetro *pcbResult* .

</dd> <dt>

*cbOutput* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbOutput* .

</dd> <dt>

*pcbResult* \[ enuncia\]
</dt> <dd>

Dirección de una variable **DWORD** que recibe el número de bytes copiados en el búfer de *pbOutput* . Si el parámetro *pbOutput* se establece en **null** cuando se llama a la función, el tamaño necesario para el búfer *pbOutput* , en bytes, se devuelve en el **valor DWORD** al que apunta este parámetro.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                    | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

La función **SslExportKey** facilita el transporte de claves de sesión de un proceso a otro, así como la exportación de la parte pública de una clave efímera.

Al exportar las claves de sesión, el tipo de BLOB es opaco, lo que significa que el formato del BLOB es irrelevante siempre que las funciones **SslExportKey** y [**SslImportKey**](sslimportkey.md) puedan interpretarlo.

Al exportar la parte pública de una clave efímera, el tipo de BLOB debe ser el tipo adecuado, como el blob **\_ público ncrypt DH \_ \_** o el **\_ \_ BLOB ECCPUBLIC ncrypt**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

