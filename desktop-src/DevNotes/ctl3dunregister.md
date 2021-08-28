---
description: Anula el registro de una aplicación como cliente de CTL3D.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Función Ctl3dUnregister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 32a954efceba7400692ad92c91bedb47283587827739c19f23e7802e1481fbe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691505"
---
# <a name="ctl3dunregister-function"></a>Función Ctl3dUnregister

Anula el registro de una aplicación como cliente de CTL3D.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prendstApp* 
</dt> <dd>

Identificador de la aplicación que se va a anular del registro como cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la aplicación no está registrada como cliente de CTL3D; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

Una aplicación que usa CTL3D debe llamar a esta función en WinMain.

Los efectos 3D no están disponibles en sistemas con una resolución inferior a VGA.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
