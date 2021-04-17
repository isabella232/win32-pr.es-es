---
description: Comprueba si los controles pueden utilizar efectos 3D.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Ctl3dEnabled función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661109"
---
# <a name="ctl3denabled-function"></a>Ctl3dEnabled función)

Comprueba si los controles pueden utilizar efectos 3D.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si los controles pueden utilizar efectos 3D; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

En Windows 4,0 o posterior, **Ctl3dEnabled** y [**Ctl3dRegister**](ctl3dregister.md) devuelven **false**.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
