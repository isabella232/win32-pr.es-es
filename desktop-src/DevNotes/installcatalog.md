---
description: Instala un catálogo en un directorio.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: Función InstallCatalog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 240754024135b5bd5aa48529d49080afbdb04e170987102346cdda2c59b12427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955934"
---
# <a name="installcatalog-function"></a>Función InstallCatalog

\[Esta función no se admite y no se debe usar.\]

Instala un catálogo en un directorio.

## <a name="syntax"></a>Sintaxis


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CatalogFullPath* \[ En\]
</dt> <dd>

Puntero a una cadena que representa la ruta de acceso completa del catálogo antes de la instalación.

</dd> <dt>

*NewBaseName* \[ in, opcional\]
</dt> <dd>

Puntero al nuevo nombre base.

</dd> <dt>

*NewCatalogFullPath* \[ out, opcional\]
</dt> <dd>

Puntero a una cadena que representa la ruta de acceso completa del catálogo después de la instalación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no está implementada actualmente, por lo que no devuelve un valor real.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
