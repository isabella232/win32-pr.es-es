---
description: Importa una clave en el proveedor de protocolo del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Función SslImportKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666956"
---
# <a name="sslimportkey-function"></a>SslImportKey función)

La función **SslImportKey** importa una clave en el proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*phKey* \[ enuncia\]
</dt> <dd>

Puntero al identificador de la [*clave criptográfica*](/windows/desktop/SecGloss/c-gly) para recibir la clave importada.

</dd> <dt>

*pszBlobType* \[ de\]
</dt> <dd>

Una cadena Unicode terminada en null que contiene un identificador que especifica el tipo de [*BLOB*](/windows/desktop/SecGloss/b-gly) que se encuentra en el búfer de *pbInput* . Puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**\_ \_ BLOB público de BCRYPT DH \_**</dt> </dl>    | Exportar una [*clave pública*](/windows/desktop/SecGloss/p-gly)de Diffie-Hellman. El búfer *pbOutput* recibe una estructura de BLOB de [**clave de BCRYPT \_ \_ \_ DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) seguida inmediatamente de los datos de clave.<br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**\_BLOB ECCPUBLIC de BCRYPT \_**</dt> </dl>     | Exportar una [*clave pública*](/windows/desktop/SecGloss/p-gly)de [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC). El búfer *pbOutput* recibe una estructura de [**\_ \_ blobs ECCKEY de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) seguida inmediatamente de los datos clave.<br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**\_BLOB de \_ clave \_ opaca de BCRYPT**</dt> </dl> | Exportar una [*clave simétrica*](/windows/desktop/SecGloss/s-gly) en un formato específico de un único proveedor de [*servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP). Los blobs opacos no se pueden transferir y se deben importar mediante el mismo CSP que generó el BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**\_BLOB RSAPUBLIC de BCRYPT \_**</dt> </dl>     | Exportar una clave pública [*RSA*](/windows/desktop/SecGloss/r-gly) . El búfer *pbOutput* recibe una estructura de [**\_ \_ blobs RSAKEY de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) seguida inmediatamente de los datos clave.<br/>                                                                                                                                                                                 |



 

</dd> <dt>

*pbKeyBlob* \[ de\]
</dt> <dd>

Puntero al búfer que contiene el BLOB de [*clave*](/windows/desktop/SecGloss/k-gly).

</dd> <dt>

*cbKeyBlob* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbKeyBlob* .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | El identificador de *hSslProvider* no es válido.<br/>                       |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *phKey* es **null**.<br/>                            |



 

## <a name="remarks"></a>Observaciones

Puede usar la función **SslImportKey** para importar claves de sesión como parte del proceso de transferencia de claves de sesión de un proceso a otro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

