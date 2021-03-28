---
description: Se envía a un archivo DLL de extensión cuando el usuario selecciona el menú de la extensión en la barra de menús del administrador de archivos. La extensión puede usar esta notificación para inicializar los elementos de menú.
title: Mensaje de FMEVENT_INITMENU (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 4bbb959feeb2c1bf99eaa999b4c51b69b0d0cf63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275110"
---
# <a name="fmevent_initmenu-message"></a>FMEVENT \_ INITMENU

Se envía a un archivo DLL de extensión cuando el usuario selecciona el menú de la extensión en la barra de menús del administrador de archivos. La extensión puede usar esta notificación para inicializar los elementos de menú.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*HMENU* 
</dt> <dd>

Identificador de la barra de menús del administrador de archivos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un archivo DLL de extensión debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Un archivo DLL de extensión recibe este mensaje solo cuando el usuario selecciona el menú de nivel superior. Si la extensión contiene submenús, debe inicializarlos al mismo tiempo que inicializa el menú de nivel superior.

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

 

 




