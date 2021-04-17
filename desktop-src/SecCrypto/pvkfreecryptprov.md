---
description: Libera el identificador de un proveedor de servicios criptográficos (CSP) y, opcionalmente, elimina el contenedor temporal creado por la función PvkGetCryptProv.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: PvkFreeCryptProv función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688428"
---
# <a name="pvkfreecryptprov-function"></a>PvkFreeCryptProv función)

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La función **PvkFreeCryptProv** libera el identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) y, opcionalmente, elimina el contenedor temporal creado por la función [**PvkGetCryptProv**](pvkgetcryptprov.md) .

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProv* \[ de\]
</dt> <dd>

Identificador para el CSP.

</dd> <dt>

*pwszCapiProvider* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null para el nombre de CSP.

</dd> <dt>

*dwProviderType* \[ de\]
</dt> <dd>

Valor **DWORD** que representa el tipo de proveedor de servicios criptográficos. Para obtener más información, vea [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md).

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
