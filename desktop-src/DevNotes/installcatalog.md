---
description: Instala un catálogo en un directorio.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: InstallCatalog función)
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
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671398"
---
# <a name="installcatalog-function"></a>InstallCatalog función)

\[Esta función no se admite y no debe usarse.\]

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

*CatalogFullPath* \[ de\]
</dt> <dd>

Puntero a una cadena que representa la ruta de acceso completa del catálogo antes de la instalación.

</dd> <dt>

*NewBaseName* \[ en, opcional\]
</dt> <dd>

Puntero al nuevo nombre base.

</dd> <dt>

*NewCatalogFullPath* \[ out, opcional\]
</dt> <dd>

Puntero a una cadena que representa la ruta de acceso completa del catálogo después de la instalación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no está implementada actualmente, por lo que no devuelve un valor real.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
