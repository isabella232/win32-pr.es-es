---
description: Controla los cambios de color del sistema para las aplicaciones que usan CTL3D.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Ctl3dColorChange función)
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
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660702"
---
# <a name="ctl3dcolorchange-function"></a>Ctl3dColorChange función)

Controla los cambios de color del sistema para las aplicaciones que usan CTL3D.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la función se ejecuta correctamente; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Se debe llamar a esta función en el procedimiento de ventana principal de la aplicación para el mensaje de **\_ SYSCOLORCHANGE de WM** , como se muestra a continuación.

## <a name="examples"></a>Ejemplos

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
