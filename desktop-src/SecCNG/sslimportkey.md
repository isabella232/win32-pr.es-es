---
description: Importa una clave en el proveedor de Capa de sockets seguros de protocolos (SSL).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Función SslImportKey (Sslprovider.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250383"
---
# <a name="sslimportkey-function"></a>Función SslImportKey

La **función SslImportKey** importa una clave en el proveedor de [*protocolos Capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

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

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*phKey* \[ out\]
</dt> <dd>

Puntero al identificador de la clave [*criptográfica para*](/windows/desktop/SecGloss/c-gly) recibir la clave importada.

</dd> <dt>

*pszBlobType* \[ En\]
</dt> <dd>

Cadena Unicode terminada en NULL que contiene un identificador que especifica el tipo de [*BLOB*](/windows/desktop/SecGloss/b-gly) contenido en el *búfer pbInput.* Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**BCRYPT \_ DH \_ PUBLIC \_ BLOB**</dt> </dl>    | Exporte un Diffie-Hellman [*clave pública*](/windows/desktop/SecGloss/p-gly). El *búfer pbOutput* recibe una estructura [**\_ BCRYPT DH KEY \_ \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) seguida inmediatamente de los datos clave.<br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**BCRYPT \_ ECCPUBLIC \_ BLOB**</dt> </dl>     | Exporte una clave pública [*de criptografía*](/windows/desktop/SecGloss/e-gly) de curva elíptica (ECC). [](/windows/desktop/SecGloss/p-gly) El *búfer pbOutput* recibe una estructura [**\_ BCRYPT ECCKEY \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) seguida inmediatamente de los datos clave.<br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**BCRYPT \_ OPAQUE \_ KEY \_ BLOB**</dt> </dl> | Exportar una [*clave simétrica*](/windows/desktop/SecGloss/s-gly) en un formato específico de un único proveedor [*de servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP). Los blobs opacos no son transferibles y deben importarse mediante el mismo CSP que generó el BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**BCRYPT \_ RSAPUBLIC \_ BLOB**</dt> </dl>     | Exportar una [*clave pública RSA.*](/windows/desktop/SecGloss/r-gly) El *búfer pbOutput* recibe una [**estructura \_ BCRYPT RSAKEY \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) inmediatamente seguida de los datos clave.<br/>                                                                                                                                                                                 |



 

</dd> <dt>

*pbKeyBlob* \[ En\]
</dt> <dd>

Puntero al búfer que contiene la [*clave BLOB*](/windows/desktop/SecGloss/k-gly).

</dd> <dt>

*cbKeyBlob* \[ En\]
</dt> <dd>

Tamaño, en bytes, del *búfer pbKeyBlob.*

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | El *identificador hSslProvider* no es válido.<br/>                       |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro phKey* es **NULL.**<br/>                            |



 

## <a name="remarks"></a>Observaciones

Puede usar la función **SslImportKey para** importar claves de sesión como parte del proceso de transferencia de claves de sesión de un proceso a otro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

