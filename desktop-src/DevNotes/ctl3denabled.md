---
description: Comprueba si los controles pueden usar efectos 3D.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Función Ctl3dEnabled
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
ms.openlocfilehash: 0d8a234736631517a0e77f5ab23f07688e3d80aa4c8b74a3b2ee51351beece90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654595"
---
# <a name="ctl3denabled-function"></a>Función Ctl3dEnabled

Comprueba si los controles pueden usar efectos 3D.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** los controles pueden usar efectos 3D; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

En Windows 4.0 o posterior, **Ctl3dEnabled** y [**Ctl3dRegister**](ctl3dregister.md) **devuelven FALSE.**

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
