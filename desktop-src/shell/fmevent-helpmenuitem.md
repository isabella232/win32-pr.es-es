---
description: Se envía a un procedimiento DLL de extensión del Administrador de archivos cuando el usuario presiona F1 en un menú o elemento de comando de la barra de herramientas. La extensión debe llamar a WinHelp, con el parámetro hwnd de esa función establecido en el valor del parámetro hwnd de la extensión.
title: FMEVENT_HELPMENUITEM mensaje (Wfext.h)
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
ms.openlocfilehash: 69078274ccd8a7a7b91bbd7bd8e8d84b3b033cec6dbcf4ce495ac2ebfd0e8381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224169"
---
# <a name="fmevent_helpmenuitem-message"></a>Mensaje \_ HELPMENUITEM de FMEVENT

Se envía a un procedimiento DLL de extensión del Administrador de archivos cuando el usuario presiona F1 en un menú o elemento de comando de la barra de herramientas. La extensión debe llamar [**a WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), con el parámetro *hwnd* de esa función establecido en el valor del *parámetro hwnd* de la extensión.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*uItem* 
</dt> <dd>

Valor que identifica el menú o elemento de comando de la barra de herramientas para el que se desea ayuda. El procedimiento de extensión usa este valor para determinar cómo llamar mejor a [**WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un procedimiento DLL de extensión debe devolver cero si procesa este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPSTRING**](fmevent-helpstring.md)
</dt> </dl>

 

 




