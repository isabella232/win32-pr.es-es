---
description: Anula el registro de una aplicación como cliente de CTL3D.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Ctl3dUnregister función)
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
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650080"
---
# <a name="ctl3dunregister-function"></a>Ctl3dUnregister función)

Anula el registro de una aplicación como cliente de CTL3D.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hinstApp* 
</dt> <dd>

Identificador de la aplicación cuya registro se va a anular como cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se anula el registro de la aplicación como cliente de CTL3D; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Una aplicación que usa CTL3D debe llamar a esta función en WinMain.

los efectos 3D no están disponibles en los sistemas que tienen una resolución inferior a VGA.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
