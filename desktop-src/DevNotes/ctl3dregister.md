---
description: Registra una aplicación como un cliente de CTL3D.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Ctl3dRegister función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650057"
---
# <a name="ctl3dregister-function"></a>Ctl3dRegister función)

Registra una aplicación como un cliente de CTL3D.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hinstApp* 
</dt> <dd>

Identificador de la aplicación que se va a registrar como cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si los efectos 3D están activos; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Una aplicación que usa CTL3D debe llamar a esta función en WinMain.

los efectos 3D no están disponibles en los sistemas que tienen una resolución inferior a VGA.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
