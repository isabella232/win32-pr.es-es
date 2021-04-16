---
description: Carga una versión especificada de un archivo DLL de biblioteca .NET Framework.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: LoadLibraryShim (función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670415"
---
# <a name="loadlibraryshim-function"></a>LoadLibraryShim (función)

Carga una versión especificada de un archivo DLL de biblioteca .NET Framework.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szDllName* \[ de\]
</dt> <dd>

Nombre del archivo DLL que se va a cargar desde el .NET Framework.

</dd> <dt>

*szVersion* \[ de\]
</dt> <dd>

Versión de la DLL que se va a cargar. Si *szVersion* es **null**, se carga la versión más reciente de la dll especificada.

</dd> <dt>

*pvReserved* 
</dt> <dd>

Reservado.

</dd> <dt>

*phModDll* \[ enuncia\]
</dt> <dd>

Identificador del módulo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función se usa para cargar los archivos dll de biblioteca que se incluyen en el paquete redistribuible de .NET Framework, no en los archivos dll generados por el usuario.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Mscoree.dll</dt> </dl> |



 

 
