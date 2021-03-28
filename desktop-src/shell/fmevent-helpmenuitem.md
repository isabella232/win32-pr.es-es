---
description: Se envía a un procedimiento DLL de extensión del administrador de archivos cuando el usuario presiona F1 en un elemento de comando de menú o barra de herramientas. La extensión debe llamar a WinHelp, con el parámetro HWND de la función establecido en el valor del parámetro HWND de la extensión.
title: Mensaje de FMEVENT_HELPMENUITEM (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: c20b5828a6e2362b9b9c13fc9b2986b0ea7b5fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984206"
---
# <a name="fmevent_helpmenuitem-message"></a>FMEVENT \_ HELPMENUITEM

Se envía a un procedimiento DLL de extensión del administrador de archivos cuando el usuario presiona F1 en un elemento de comando de menú o barra de herramientas. La extensión debe llamar a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), con el parámetro *hWnd* de la función establecido en el valor del parámetro *hWnd* de la extensión.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*uItem* 
</dt> <dd>

Valor que identifica el elemento de comando de menú o de la barra de herramientas para el que se desea obtener ayuda. El procedimiento de extensión usa este valor para determinar el mejor modo de llamar a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un procedimiento de archivo DLL de extensión debe devolver cero si procesa este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPSTRING**](fmevent-helpstring.md)
</dt> </dl>

 

 




