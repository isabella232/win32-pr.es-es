---
description: Se envía a un archivo DLL de extensión cuando el Administrador de archivos descarga el archivo DLL.
title: FMEVENT_UNLOAD mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 5d18d72a43ac1fca6906bb1e3f7a14468dbd02933d801dc3c20e2a933bc18f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860370"
---
# <a name="fmevent_unload-message"></a>Mensaje UNLOAD de FMEVENT \_

Se envía a un archivo DLL de extensión cuando el Administrador de archivos descarga el archivo DLL.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un archivo DLL de extensión debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Es posible que los valores *hwnd* y **hMenu** pasados con los mensajes [**\_ FMEVENT LOAD**](fmevent-load.md) y [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) no sean válidos en el momento de enviar este mensaje.

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

 

 




