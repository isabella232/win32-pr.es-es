---
description: 'Notifica al objeto de devolución de llamada que se está actualizando la barra de estado. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_UPDATESTATUSBAR (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997773"
---
# <a name="sfvm_updatestatusbar-message"></a>SFVM \_ UPDATESTATUSBAR

Notifica al objeto de devolución de llamada que se está actualizando la barra de estado. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fInitialize* \[ de\]
</dt> <dd>

Valor **booleano** que se establece en **true** si se está inicializando la barra de estado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando reciba esta notificación:

-   Vuelva a \_ Aceptar si va a controlar la actualización.
-   Devuelve MAKE \_ HRESULT (Severity \_ Success, 0, 1) para que el objeto de vista de carpeta del sistema establezca el texto de la barra de estado.
-   Devolver E \_ no puede hacer que el objeto de vista de carpeta del sistema controle la barra de estado.

El texto predeterminado de la barra de estado es el siguiente.



| Estado                      | Texto de la barra de estado                         |
|-----------------------------|-----------------------------------------|
| No hay elementos seleccionados           | " \# \# objetos" (en la carpeta)          |
| Un elemento seleccionado           | El recuadro informativo para el elemento, si está disponible. |
| Hay más de un elemento seleccionado | " \# \# objetos seleccionados"                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
