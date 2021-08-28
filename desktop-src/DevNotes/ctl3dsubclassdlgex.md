---
description: Subclasesa todos los controles de un cuadro de diálogo y de la propia ventana de diálogo.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Función Ctl3dSubclassDlgEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: aeacdf75e20e2d3521405c20b52d29a466c5fe9a063d70e5acb3c0597934ab9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162136"
---
# <a name="ctl3dsubclassdlgex-function"></a>Función Ctl3dSubclassDlgEx

Subclasesa todos los controles de un cuadro de diálogo y de la propia ventana de diálogo.

## <a name="syntax"></a>Sintaxis


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndDlg* 
</dt> <dd>

Identificador de la ventana de diálogo.

</dd> <dt>

*grbit* 
</dt> <dd>

Tipos de control que se deben crear subclases. Este valor puede ser cualquiera de los siguientes.



| Valor                                                                                                                                                                                                                                     | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <dt>**CTL3D \_ Botones**</dt> <dt>0x0001</dt> </dl>                 | Botones de subclase.<br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <dt>**CTL3D \_ LISTBOXES**</dt> <dt>0x0002</dt> </dl>           | Cuadros de lista de subclase.<br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <dt>**CTL3D \_ EDITS**</dt> <dt>0x0004</dt> </dl>                       | Controles de edición de subclase.<br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <dt>**CTL3D \_ Combos**</dt> <dt>0x0008</dt> </dl>                    | Cuadros combinados de subclase.<br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <dt>**CTL3D \_ StaticTEXTS**</dt> <dt>0x0010</dt> </dl>     | Controles de texto estático de subclase.<br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <dt>**CTL3D \_ StaticFRAMES**</dt> <dt>0x0020</dt> </dl>  | Fotogramas estáticos de subclase.<br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <dt>**CTL3D \_ TODOS**</dt> <dt>los 0xffff</dt> </dl>                             | Subclase de todos los controles.<br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <dt>**CTL3D \_ NODLGWINDOW**</dt> <dt>0x00010000</dt> </dl> | No subclase la ventana de diálogo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza correctamente; de lo contrario, devuelve **FALSE.**

## <a name="remarks"></a>Comentarios

Esta función es especialmente útil en aplicaciones basadas en C++.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
