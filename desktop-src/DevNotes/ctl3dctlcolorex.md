---
description: Controla el mensaje \_ WM CTLCOLOR para las aplicaciones que usan CTL3D.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Función Ctl3dCtlColorEx
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
ms.openlocfilehash: 46fe35fd507f20e41e0a9b563ded5c9cf46e9c557893bc9287d65cbdf651b24f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691645"
---
# <a name="ctl3dctlcolorex-function"></a>Función Ctl3dCtlColorEx

Controla el **mensaje \_ WM CTLCOLOR** para las aplicaciones que usan CTL3D.

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

Mensaje **WM \_ CTLCOLOR** para la aplicación.

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

Devuelve un identificador al pincel adecuado si la función se realiza correctamente; de lo contrario, `(HBRUSH)(0)` devuelve un valor que indica que se ha producido un error.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
