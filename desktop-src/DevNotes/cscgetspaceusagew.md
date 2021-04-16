---
description: Recupera información sobre el espacio utilizado por la memoria caché de Archivos sin conexión.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: CSCGetSpaceUsageW función)
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
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650009"
---
# <a name="cscgetspaceusagew-function"></a>CSCGetSpaceUsageW función)

\[Esta función no se admite y no debe usarse.\]

Recupera información sobre el espacio utilizado por la memoria caché de Archivos sin conexión.

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

*dwSize* \[ de\]
</dt> <dd>

Tamaño del búfer de *lptzLocation* , en caracteres.

</dd> <dt>

*lpdwMaxSpaceHigh* \[ in, out\]
</dt> <dd>

**Valor DWORD** de orden superior del número máximo de bytes disponibles en la memoria caché.

</dd> <dt>

*lpdwMaxSpaceLow* \[ in, out\]
</dt> <dd>

**Valor DWORD** de orden inferior del número máximo de bytes disponibles en la memoria caché.

</dd> <dt>

*lpdwCurrentSpaceHigh* \[ in, out\]
</dt> <dd>

**Valor DWORD** de orden superior del número actual de bytes disponibles en la memoria caché.

</dd> <dt>

*lpdwCurrentSpaceLow* \[ in, out\]
</dt> <dd>

**Valor DWORD** de orden inferior del número actual de bytes disponibles en la memoria caché.

</dd> <dt>

*lpcntTotalFiles* \[ in, out\]
</dt> <dd>

Número total de archivos en la memoria caché.

</dd> <dt>

*lpcntTotalDirs* \[ in, out\]
</dt> <dd>

El número total de directorios en la memoria caché.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
