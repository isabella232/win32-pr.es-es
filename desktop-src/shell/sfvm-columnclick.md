---
description: 'Notifica al objeto de devolución de llamada que el usuario ha haga clic en un encabezado de columna para ordenar la lista de objetos en la vista de carpetas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_COLUMNCLICK (ShlObj. h)
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
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497890"
---
# <a name="sfvm_columnclick-message"></a>SFVM \_ COLUMNCLICK

Notifica al objeto de devolución de llamada que el usuario ha haga clic en un encabezado de columna para ordenar la lista de objetos en la vista de carpetas. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iColumn* \[ de\]
</dt> <dd>

Índice de la columna en la que se hizo clic.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En respuesta a esta notificación, debe devolver S \_ OK para reorganizar la lista. Para que el objeto de vista de carpeta del sistema reorganice la lista, devuelva S \_ false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
