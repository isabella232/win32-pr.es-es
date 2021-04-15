---
description: Comprueba un solo archivo de catálogo.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: VerifyCatalogFile función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649499"
---
# <a name="verifycatalogfile-function"></a>VerifyCatalogFile función)

\[Esta función no se admite y no debe usarse.\]

Comprueba un solo archivo de catálogo.

## <a name="syntax"></a>Sintaxis


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CatalogFullPath* 
</dt> <dd>

Ruta de acceso completa del archivo de catálogo que se va a comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve el **error \_ Success**; de lo contrario, devuelve el error de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

Si el catálogo es un catálogo firmado con Authenticode, esta función devuelve un **error de \_ \_ \_ Editor de confianza Authenticode** si se realiza correctamente; de lo contrario, devuelve el **error no se \_ \_ \_ ha \_ establecido la confianza Authenticode**.

Si la función no puede determinar si el publicador es de confianza, también puede devolver un error no **\_ identificado \_**.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
