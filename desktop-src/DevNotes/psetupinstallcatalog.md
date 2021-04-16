---
description: Instala un archivo de catálogo.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: pSetupInstallCatalog función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649959"
---
# <a name="psetupinstallcatalog-function"></a>pSetupInstallCatalog función)

\[Esta función ya no es compatible con Microsoft. Los desarrolladores deben usar **CryptCATAdminAddCatalog**.\]

Instala un archivo de catálogo.

## <a name="syntax"></a>Sintaxis


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CatalogFullPath* \[ de\]
</dt> <dd>

Ruta de acceso completa del catálogo que se va a instalar en el sistema.

</dd> <dt>

*NewBaseName* \[ de\]
</dt> <dd>

Nuevo nombre base que se utilizará cuando se copie el archivo de catálogo en el almacén de catálogos.

</dd> <dt>

*NewCatalogFullPath* \[ out, opcional\]
</dt> <dd>

Opcionalmente, recibe la ruta de acceso completa del archivo de catálogo en el almacén de catálogos. Este búfer debe ser al menos **una \_ ruta de acceso máxima** de bytes (versión ANSI) o chars (versión Unicode).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, **no devuelve ningún \_ error**; de lo contrario, devuelve un código de error de Win32 que indica la causa del error.

## <a name="remarks"></a>Observaciones

El sistema copia el archivo en un directorio especial y, de forma opcional, se le cambia el nombre.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CryptCATAdminAddCatalog**](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
