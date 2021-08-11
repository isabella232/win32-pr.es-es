---
description: Enviado por una extensión del Administrador de archivos (u otra aplicación) para que el Administrador de archivos vuelva a cargar todos los archivos DLL de extensión enumerados en la sección Complementos del Winfile.ini \[ \] archivo.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: FM_RELOAD_EXTENSIONS mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e4e632ac153a78e729ce0d3fcd65f49ae90781bd29cfe354d4571ba04e63be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224179"
---
# <a name="fm_reload_extensions-message"></a>Mensaje \_ DE EXTENSIONES DE RECARGA DE \_ FM

Enviado por una extensión del Administrador de archivos (u otra aplicación) para que el Administrador de archivos vuelva a cargar todos los archivos DLL de extensión enumerados en la sección Complementos del Winfile.ini \[ \] archivo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Otras aplicaciones pueden usar la [**función PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para enviar este mensaje al Administrador de archivos. Para obtener el identificador de ventana del Administrador de archivos adecuado, una aplicación puede especificar "WFS Frame" como el parámetro \_ *lpszClassName* en una llamada a la [**función FindWindow.**](/windows/win32/api/winuser/nf-winuser-findwindowa)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulta también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
