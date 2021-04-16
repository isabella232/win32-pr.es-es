---
description: Controla el \_ mensaje de CTLCOLOR de WM para las aplicaciones que usan CTL3D.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Ctl3dCtlColorEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650039"
---
# <a name="ctl3dctlcolorex-function"></a>Ctl3dCtlColorEx función)

Controla el mensaje de **\_ CTLCOLOR de WM** para las aplicaciones que usan CTL3D.

## <a name="syntax"></a>Sintaxis


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wm* 
</dt> <dd>

Mensaje **de \_ CTLCOLOR de WM** para la aplicación.

</dd> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto de presentación (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de una ventana secundaria (control).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador al pincel adecuado si la función se ejecuta correctamente; de lo contrario, devuelve que `(HBRUSH)(0)` indica que se ha producido un error.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
