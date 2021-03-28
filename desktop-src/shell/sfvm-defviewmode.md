---
description: 'Permite que el objeto de devolución de llamada especifique el modo de vista. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_DEFVIEWMODE (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8d57bb61b2b938947d0290345215e3735d9d8763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997921"
---
# <a name="sfvm_defviewmode-message"></a>SFVM \_ DEFVIEWMODE

Permite que el objeto de devolución de llamada especifique el modo de vista. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pViewMode* \[ enuncia\]
</dt> <dd>

Uno de los valores del tipo enumerado [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
