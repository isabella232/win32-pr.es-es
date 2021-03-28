---
description: SFVM \_ THISIDLIST puede modificarse o no estar disponible.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Mensaje de SFVM_THISIDLIST (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818619"
---
# <a name="sfvm_thisidlist-message"></a>SFVM \_ THISIDLIST

\[**SFVM \_ THISIDLIST** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Permite que el objeto de devolución de llamada especifique el puntero de la vista a una lista de identificadores de elemento (PIDL). Solo se usa cuando se ha producido un error en [**IPersistIDList:: SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) y [**IPersistFolder2:: GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) . Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PIDL* \[ enuncia\]
</dt> <dd>

Dirección de PIDL de la vista.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
