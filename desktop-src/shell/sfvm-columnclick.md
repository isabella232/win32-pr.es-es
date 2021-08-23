---
description: Notifica al objeto de devolución de llamada que el usuario ha hecho clic en un encabezado de columna para ordenar la lista de objetos en la vista de carpeta. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_COLUMNCLICK mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d5ebd98ebc887d26bcee4799ffa3412df803fd0dfa099ac41bc69e1c25d83f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592705"
---
# <a name="sfvm_columnclick-message"></a>Mensaje \_ COLUMNCLICK de SFVM

Notifica al objeto de devolución de llamada que el usuario ha hecho clic en un encabezado de columna para ordenar la lista de objetos en la vista de carpeta. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iColumn* \[ En\]
</dt> <dd>

Índice de la columna en la que se hizo clic.

</dd> </dl>

## <a name="remarks"></a>Comentarios

En respuesta a esta notificación, debe devolver S \_ OK para reorganizar la lista usted mismo. Para que el objeto de vista de carpetas del sistema reordene la lista, devuelva S \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
