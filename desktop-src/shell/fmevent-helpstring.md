---
description: Se envía a un procedimiento de archivo DLL de extensión del administrador de archivos cuando el administrador de archivos desea una cadena de ayuda para un elemento de comando de menú o barra de herramientas.
title: Mensaje de FMEVENT_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: ae3be1953d4c8bbf70f8f17fcf34fcfb1ac583f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276761"
---
# <a name="fmevent_helpstring-message"></a>FMEVENT el \_ mensaje de HELPSTRING

Se envía a un procedimiento de archivo DLL de extensión del administrador de archivos cuando el administrador de archivos desea una cadena de ayuda para un elemento de comando de menú o barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lpfmshs* 
</dt> <dd>

La dirección de una estructura [**FMS \_ HELPSTRING**](fms-helpstring.md) que comunica los datos de la cadena de ayuda de los elementos de comando. La estructura **FMS \_ HELPSTRING** identifica el elemento de comando para el que se desea una cadena de ayuda, junto con un identificador de su menú. Después, una aplicación escribe la cadena de ayuda adecuada en el miembro **szHelp** de la estructura **FMS \_ HELPSTRING** .

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

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




