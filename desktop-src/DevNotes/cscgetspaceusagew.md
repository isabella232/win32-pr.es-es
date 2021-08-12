---
description: Recupera información sobre el espacio utilizado por la caché Archivos sin conexión datos.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: Función CSCGetSpaceUsageW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 8dd6d12c4e0267c97b93a812a4b66d3bd14a408dff0191686d4949ccbc958723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667958"
---
# <a name="cscgetspaceusagew-function"></a>Función CSCGetSpaceUsageW

\[Esta función no se admite y no se debe usar.\]

Recupera información sobre el espacio utilizado por la caché Archivos sin conexión datos.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lptzLocation* \[ in, out\]
</dt> <dd>

Ubicación del directorio de la memoria caché.

</dd> <dt>

*dwSize* \[ En\]
</dt> <dd>

Tamaño del búfer *lptzLocation,* en caracteres.

</dd> <dt>

*lpdwMaxSpaceHigh* \[ in, out\]
</dt> <dd>

DWORD de **orden superior** del número máximo de bytes disponibles en la memoria caché.

</dd> <dt>

*lpdwMaxSpaceLow* \[ in, out\]
</dt> <dd>

DWORD de  orden bajo del número máximo de bytes disponibles en la memoria caché.

</dd> <dt>

*lpdwCurrentSpaceHigh* \[ in, out\]
</dt> <dd>

DWORD de orden **superior** del número actual de bytes disponibles en la memoria caché.

</dd> <dt>

*lpdwCurrentSpaceLow* \[ in, out\]
</dt> <dd>

DWORD de orden **bajo** del número actual de bytes disponibles en la memoria caché.

</dd> <dt>

*lpcntTotalFiles* \[ in, out\]
</dt> <dd>

Número total de archivos de la memoria caché.

</dd> <dt>

*lpcntTotalDirs* \[ in, out\]
</dt> <dd>

Número total de directorios de la memoria caché.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** se realiza correctamente; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
