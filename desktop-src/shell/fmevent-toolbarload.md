---
description: Se envía a un archivo DLL de extensión cuando el Administrador de archivos carga su barra de herramientas. Este mensaje permite que un archivo DLL de extensión agregue un botón a la barra de herramientas del Administrador de archivos.
title: FMEVENT_TOOLBARLOAD mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: c4195acedbd696679a2deea2f4d6e268717566d1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841276"
---
# <a name="fmevent_toolbarload-message"></a>MENSAJE DE DESCARGA \_ DE LA BARRA DE HERRAMIENTAS DE FMEVENT

Se envía a un archivo DLL de extensión cuando el Administrador de archivos carga su barra de herramientas. Este mensaje permite que un archivo DLL de extensión agregue un botón a la barra de herramientas del Administrador de archivos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lpfmstbl* 
</dt> <dd>

Dirección de una estructura [**\_ TOOLBARLOAD de FMS.**](fms-toolbarload.md) Si el archivo DLL de extensión agrega un botón a la barra de herramientas del Administrador de archivos, el archivo DLL debe rellenar la estructura con información sobre el botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un archivo DLL de extensión debe devolver **TRUE** para agregar el botón a la barra de herramientas. Si el archivo DLL devuelve **FALSE,** el Administrador de archivos no agrega el botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




