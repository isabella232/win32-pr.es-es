---
description: Se envía a un archivo DLL de extensión cuando el administrador de archivos está cargando su barra de herramientas. Este mensaje permite a un archivo DLL de extensión agregar un botón a la barra de herramientas del administrador de archivos.
title: Mensaje de FMEVENT_TOOLBARLOAD (Wfext. h)
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
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276760"
---
# <a name="fmevent_toolbarload-message"></a>FMEVENT \_ TOOLBARLOAD

Se envía a un archivo DLL de extensión cuando el administrador de archivos está cargando su barra de herramientas. Este mensaje permite a un archivo DLL de extensión agregar un botón a la barra de herramientas del administrador de archivos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lpfmstbl* 
</dt> <dd>

Dirección de una estructura [**de \_ TOOLBARLOAD de FMS**](fms-toolbarload.md) . Si el archivo DLL de extensión agrega un botón a la barra de herramientas en el administrador de archivos, el archivo DLL debe rellenar la estructura con información acerca del botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un archivo DLL de extensión debe devolver **true** para agregar el botón a la barra de herramientas. Si el archivo DLL devuelve **false**, el administrador de archivos no agrega el botón.

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

 

 




