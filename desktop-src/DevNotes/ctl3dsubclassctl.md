---
description: Subclases de un control individual a menos que el control aparezca en un cuadro de diálogo.
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Ctl3dSubclassCtl función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0ff6c6744c4ddda203149981218b8143fb78bce7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650056"
---
# <a name="ctl3dsubclassctl-function"></a>Ctl3dSubclassCtl función)

Subclases de un control individual a menos que el control aparezca en un cuadro de diálogo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana de control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el control se ha subclase correctamente; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ctl3dUnsubclassCtl**](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
