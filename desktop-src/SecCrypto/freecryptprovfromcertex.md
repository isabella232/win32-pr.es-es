---
description: 'Libera el identificador de un proveedor de servicios criptográficos (CSP) o de una clave Cryptography API: Next Generation (CNG).'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: FreeCryptProvFromCertEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912038"
---
# <a name="freecryptprovfromcertex-function"></a>FreeCryptProvFromCertEx función)

La función **FreeCryptProvFromCertEx** libera el identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) o de una clave Cryptography API: Next Generation (CNG).

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fAcquired* \[ de\]
</dt> <dd>

Valor que especifica si el identificador del proveedor se adquirió del [*certificado*](../secgloss/c-gly.md).

</dd> <dt>

*hProv* \[ de\]
</dt> <dd>

Identificador de un CSP de CAPICOM o un identificador para una clave CNG.

</dd> <dt>

*dwKeySpec* 
</dt> <dd>

Dirección de una variable **DWORD** que recibe información adicional sobre la clave. Puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                | Significado                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**EN \_ KEYEXCHANGE**</dt> </dl>                     | El par de claves es un par de intercambio de claves.<br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**EN la \_ Signatura**</dt> </dl>                           | El par de claves es un par de firmas.<br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <dt>**\_especificación de \_ clave del NCRYPT de CERT \_**</dt> </dl> | La clave es una clave CNG.<br/> **Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |



 

</dd> <dt>

*pwszCapiProvider* \[ en, opcional\]
</dt> <dd>

Puntero a una cadena terminada en null para el nombre del proveedor.

</dd> <dt>

*dwProviderType* \[ de\]
</dt> <dd>

Especifica el tipo de CSP. Puede ser cero o uno de los [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md). Si este miembro es cero, el contenedor de claves es uno de los proveedores de almacenamiento de claves CNG.

</dd> <dt>

*pwszTmpContainer* \[ en, opcional\]
</dt> <dd>

Un puntero a una cadena terminada en null para el nombre del contenedor de claves temporal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
