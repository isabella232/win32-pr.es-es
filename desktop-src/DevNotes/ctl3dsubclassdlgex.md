---
description: Subclases de todos los controles de un cuadro de diálogo y de la propia ventana de diálogo.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Ctl3dSubclassDlgEx función)
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
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650119"
---
# <a name="ctl3dsubclassdlgex-function"></a>Ctl3dSubclassDlgEx función)

Subclases de todos los controles de un cuadro de diálogo y de la propia ventana de diálogo.

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

Identificador de la ventana de cuadro de diálogo.

</dd> <dt>

*grbit* 
</dt> <dd>

Tipos de control de los que se van a crear subclases. Este valor puede ser cualquiera de los siguientes.



| Value                                                                                                                                                                                                                                     | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <dt>**CTL3D \_ BOTONES**</dt> <dt>0x0001</dt> </dl>                 | Botones de subclase.<br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <dt>**CTL3D \_ LISTBOXs**</dt> <dt>0x0002</dt> </dl>           | Cuadros de lista de subclases.<br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <dt>**CTL3D \_ EDITA**</dt> <dt>0x0004</dt> </dl>                       | Controles de edición de subclase.<br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <dt>**CTL3D \_**</dt> <dt>0x0008</dt> combinados </dl>                    | Cuadros combinados de subclase.<br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <dt>**CTL3D \_ STATICTEXTS**</dt> <dt>0x0010</dt> </dl>     | Controles de texto estático de subclase.<br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <dt>**CTL3D \_ STATICFRAMES**</dt> <dt>0x0020</dt> </dl>  | Marcos estáticos de subclase.<br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <dt>**CTL3D \_ TODO**</dt> <dt>0xFFFF</dt> </dl>                             | Subclase de todos los controles.<br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <dt>**CTL3D \_ NODLGWINDOW**</dt> <dt>0x00010000</dt> </dl> | No debe subclaser la ventana de cuadro de diálogo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la función se ejecuta correctamente; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Esta función es especialmente útil en aplicaciones basadas en C++.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
