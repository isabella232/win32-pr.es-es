---
description: Se envía a un archivo DLL de extensión cuando el Administrador de archivos carga el archivo DLL.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: FMEVENT_LOAD mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 8001ca861b77755ea7f5ee829a9af490c2f426dcd6179f2fe84831c624bb4ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860660"
---
# <a name="fmevent_load-message"></a>Mensaje DE \_ CARGA DE FMEVENT

Se envía a un archivo DLL de extensión cuando el Administrador de archivos carga el archivo DLL.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lpfmsld* 
</dt> <dd>

Dirección de una estructura [**LOAD \_ de FMS**](fms-load.md) que especifica el valor delta del elemento de menú.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un archivo DLL de extensión debe devolver **TRUE** para continuar cargando el archivo DLL. Si el archivo DLL devuelve **FALSE,** el Administrador de archivos llama a la [**función FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) y finaliza cualquier comunicación con el archivo DLL de extensión.

## <a name="remarks"></a>Comentarios

Una aplicación debe rellenar los **miembros dwSize**, **szMenuName** y **hMenu** en la [**estructura LOAD \_ de FMS.**](fms-load.md) También debe guardar el valor del miembro **wMenuDelta** y usarlo para identificar los elementos de menú al modificar el menú.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
