---
description: Enviado por una extensión del administrador de archivos (u otra aplicación) para que el administrador de archivos vuelva a cargar todos los archivos dll de extensión enumerados en la \[ \] sección de complementos del archivo de Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: Mensaje de FM_RELOAD_EXTENSIONS (Wfext. h)
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
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985518"
---
# <a name="fm_reload_extensions-message"></a>Mensaje de extensión de \_ recarga de FM \_

Enviado por una extensión del administrador de archivos (u otra aplicación) para que el administrador de archivos vuelva a cargar todos los archivos dll de extensión enumerados en la \[ \] sección de complementos del archivo de Winfile.ini.

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

## <a name="remarks"></a>Observaciones

Otras aplicaciones pueden usar la función [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para enviar este mensaje al administrador de archivos. Para obtener el identificador de ventana del administrador de archivos adecuado, una aplicación puede especificar "ft \_ frame" como el parámetro *lpszClassName* en una llamada a la función [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
