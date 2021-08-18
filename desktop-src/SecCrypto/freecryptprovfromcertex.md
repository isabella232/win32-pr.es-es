---
description: 'Libera el identificador a un proveedor de servicios criptográficos (CSP) o a una clave cryptography API: Next Generation (CNG).'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: Función FreeCryptProvFromCertEx
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
ms.openlocfilehash: b887fd7cd37e8963430378590552273b0856dc2cf73e9d0da15ab41a5a622447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006743"
---
# <a name="freecryptprovfromcertex-function"></a>Función FreeCryptProvFromCertEx

La **función FreeCryptProvFromCertEx** libera el identificador [*a*](../secgloss/c-gly.md) un proveedor de servicios criptográficos (CSP) o a una clave cryptography API: Next Generation (CNG).

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*fAcquired* \[ En\]
</dt> <dd>

Valor que especifica si el identificador del proveedor se adquirió del [*certificado*](../secgloss/c-gly.md).

</dd> <dt>

*hProv* \[ En\]
</dt> <dd>

Un identificador para un CSP capicom o un identificador para una clave CNG.

</dd> <dt>

*dwKeySpec* 
</dt> <dd>

Dirección de una variable **DWORD** que recibe información adicional sobre la clave. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                | Significado                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**AT \_ KEYEXCHANGE**</dt> </dl>                     | El par de claves es un par de intercambio de claves.<br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**AT \_ SIGNATURE**</dt> </dl>                           | El par de claves es un par de firmas.<br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <dt>**CERT \_ NCRYPT \_ KEY \_ SPEC**</dt> </dl> | La clave es una clave CNG.<br/> **Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |



 

</dd> <dt>

*pwszCapiProvider* \[ in, opcional\]
</dt> <dd>

Puntero a una cadena terminada en NULL para el nombre del proveedor.

</dd> <dt>

*dwProviderType* \[ En\]
</dt> <dd>

Especifica el tipo de CSP. Puede ser cero o uno de los tipos [de proveedor de servicios criptográficos](cryptographic-provider-types.md). Si este miembro es cero, el contenedor de claves es uno de los proveedores de almacenamiento de claves CNG.

</dd> <dt>

*pwszTmpContainer* \[ in, opcional\]
</dt> <dd>

Puntero a una cadena terminada en NULL para el nombre del contenedor de claves temporal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
