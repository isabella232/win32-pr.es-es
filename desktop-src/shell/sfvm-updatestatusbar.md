---
description: Notifica al objeto de devolución de llamada que se está actualizando la barra de estado. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_UPDATESTATUSBAR mensaje (Shlobj.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466281"
---
# <a name="sfvm_updatestatusbar-message"></a>Mensaje \_ UPDATESTATUSBAR de SFVM

Notifica al objeto de devolución de llamada que se está actualizando la barra de estado. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fInitialize* \[ En\]
</dt> <dd>

Valor **BOOL** que se establece en **TRUE** si se inicializa la barra de estado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando reciba esta notificación:

-   Devuelve S \_ OK si va a controlar la actualización.
-   Devuelve MAKE \_ HRESULT(SEVERITY SUCCESS,0,1) para que el objeto de vista de carpeta del sistema \_ establezca el texto de la barra de estado.
-   Devuelve E \_ FAIL para que el objeto de vista de carpeta del sistema controle la barra de estado.

El texto predeterminado de la barra de estado es el siguiente.



| Status                      | Texto de la barra de estado                         |
|-----------------------------|-----------------------------------------|
| No hay elementos seleccionados           | " \# \# objects" (en la carpeta )          |
| Un elemento seleccionado           | Información sobre el elemento, si está disponible. |
| Más de un elemento seleccionado | " \# \# objetos seleccionados"                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
