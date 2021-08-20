---
description: Desactiva las subclases para el control especificado.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Función Ctl3dUnsubclassCtl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: db0f87b7aec956a74a0c54871da4019c1ddd4f1bcd57fce3806218003fcb70bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162126"
---
# <a name="ctl3dunsubclassctl-function"></a>Función Ctl3dUnsubclassCtl

Desactiva las subclases para el control especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador de la ventana de control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el control se ha subclasificado correctamente; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ctl3dSubclassCtl**](ctl3dsubclassctl.md)
</dt> </dl>

 

 
