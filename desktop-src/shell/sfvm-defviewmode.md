---
description: Permite que el objeto de devolución de llamada especifique el modo de vista. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_DEFVIEWMODE mensaje (Shlobj.h)
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
ms.openlocfilehash: 28958fd992f70924ebbd51c06090d3a55c0ef8e6418d1ee055c5eb534acb9d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090165"
---
# <a name="sfvm_defviewmode-message"></a>Mensaje \_ SFVM DEFVIEWMODE

Permite que el objeto de devolución de llamada especifique el modo de vista. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pViewMode* \[ out\]
</dt> <dd>

Uno de los valores del tipo [**enumerado FOLDERVIEWMODE.**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
