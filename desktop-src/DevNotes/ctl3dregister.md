---
description: Registra una aplicación como cliente de CTL3D.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Función Ctl3dRegister
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
ms.openlocfilehash: 9f58236891b8a673102905e0ef0c108ac9da6e6192788abea9c6e79baf8acfcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162163"
---
# <a name="ctl3dregister-function"></a>Función Ctl3dRegister

Registra una aplicación como cliente de CTL3D.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prendstApp* 
</dt> <dd>

Identificador de la aplicación que se va a registrar como cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** los efectos 3D están activos; de lo contrario, devuelve **FALSE.**

## <a name="remarks"></a>Comentarios

Una aplicación que use CTL3D debe llamar a esta función en WinMain.

Los efectos 3D no están disponibles en sistemas con una resolución inferior a VGA.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
