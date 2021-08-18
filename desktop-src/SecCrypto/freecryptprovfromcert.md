---
description: Libera el identificador a un proveedor de servicios criptográficos (CSP) y, opcionalmente, elimina el contenedor temporal creado por la función GetCryptProvFromCert.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: Función FreeCryptProvFromCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8797a6f48bcfb973a6c07a4b05ae0d39bc3b4522ab6f7ae70a80eaa77081da44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006793"
---
# <a name="freecryptprovfromcert-function"></a>Función FreeCryptProvFromCert

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La **función FreeCryptProvFromCert** libera el identificador [*a*](../secgloss/c-gly.md) un proveedor de servicios criptográficos (CSP) y, opcionalmente, elimina el contenedor temporal creado por la función [**GetCryptProvFromCert.**](getcryptprovfromcert.md)

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
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

Puntero a una [**estructura HCRYPTPROV**](hcryptprov.md) para el CSP.

</dd> <dt>

*pwszCapiProvider* \[ en, opcional\]
</dt> <dd>

Puntero a una cadena terminada en NULL para el nombre del proveedor.

</dd> <dt>

*dwProviderType* \[ En\]
</dt> <dd>

Especifica el tipo de CSP. Puede ser cero o uno de los tipos [de proveedor de servicios criptográficos](cryptographic-provider-types.md). Si este miembro es cero, el contenedor de claves es uno de los proveedores de almacenamiento de claves CNG.

</dd> <dt>

*pwszTmpContainer* \[ en, opcional\]
</dt> <dd>

Puntero a una cadena terminada en NULL para el nombre del contenedor de claves temporal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
