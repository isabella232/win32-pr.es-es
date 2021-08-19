---
description: Comprueba un único archivo de catálogo.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: Función VerifyCatalogFile
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
ms.openlocfilehash: eb4012a04b4da9e353a5d771f9b9e61d4bfba8b45ed6a7d5c65a81c197ff9be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075749"
---
# <a name="verifycatalogfile-function"></a>Función VerifyCatalogFile

\[Esta función no se admite y no se debe usar.\]

Comprueba un único archivo de catálogo.

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

Si la función se realiza correctamente, devuelve **ERROR \_ SUCCESS;** de lo contrario, devuelve el error de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

Si el catálogo es un catálogo firmado por Authenticode, esta función devuelve **ERROR \_ AUTHENTICODE \_ TRUSTED \_ PUBLISHER** si se realiza correctamente; de lo contrario, devuelve **ERROR \_ AUTHENTICODE \_ TRUST NOT \_ \_ ESTABLISHED**.

Si la función no puede determinar si el publicador es de confianza, también puede devolver **ERROR \_ UNIDENTIFIED \_ ERROR**.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
