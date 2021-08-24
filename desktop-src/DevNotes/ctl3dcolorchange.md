---
description: Controla los cambios de color del sistema para las aplicaciones que usan CTL3D.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Función Ctl3dColorChange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: c9c3032bb7105a27b995c236e01ce5fc5c304de4108f6c996a5cbb5799be496d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654605"
---
# <a name="ctl3dcolorchange-function"></a>Función Ctl3dColorChange

Controla los cambios de color del sistema para las aplicaciones que usan CTL3D.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza correctamente; de lo contrario, devuelve **FALSE.**

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

Se debe llamar a esta función en el procedimiento de ventana principal de la aplicación para el mensaje **\_ SYSCOLORCHANGE** de WM, como se muestra a continuación.

## <a name="examples"></a>Ejemplos

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
