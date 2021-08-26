---
description: Carga una versión especificada de un archivo DLL .NET Framework biblioteca.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: Función LoadLibraryShim
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
ms.openlocfilehash: 123d4036713d6c1c5b7f7a08026d29d7d34126c28c5c2c1fceb94eb01baf9609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001245"
---
# <a name="loadlibraryshim-function"></a>Función LoadLibraryShim

Carga una versión especificada de un archivo DLL .NET Framework biblioteca.

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

*szDllName* \[ En\]
</dt> <dd>

Nombre del archivo DLL que se va a cargar desde el .NET Framework.

</dd> <dt>

*szVersion* \[ En\]
</dt> <dd>

Versión del archivo DLL que se va a cargar. Si *szVersion* es **NULL,** se carga la versión más reciente del archivo DLL especificado.

</dd> <dt>

*pvReserved* 
</dt> <dd>

Reservado.

</dd> <dt>

*phModDll* \[ out\]
</dt> <dd>

Identificador del módulo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función se usa para cargar archivos DLL de biblioteca que se incluyen en .NET Framework paquete redistribuible, no archivos DLL generados por el usuario.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Mscoree.dll</dt> </dl> |



 

 
