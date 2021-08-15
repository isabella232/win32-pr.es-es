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
ms.openlocfilehash: a8aba636910735e9baa0bd3ebbcf846ecf69a2174b56372a387b541c92e59732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860397"
---
# <a name="fmevent_toolbarload-message"></a>FMEVENT \_ TOOLBARLOAD message

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

Un archivo DLL de extensión debe devolver **TRUE** para agregar el botón a la barra de herramientas. Si el archivo DLL devuelve **FALSE**, el Administrador de archivos no agrega el botón .

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

 

 




