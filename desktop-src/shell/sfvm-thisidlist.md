---
description: SFVM \_ THISIDLIST puede modificarse o no estar disponible.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: SFVM_THISIDLIST mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd00f1cfc2b6661dac2414f0327cab03d4c0586eb62b992b5e33f81e64565246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968634"
---
# <a name="sfvm_thisidlist-message"></a>Mensaje \_ THISIDLIST de SFVM

\[**SFVM \_ THISIDLIST** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Permite que el objeto de devolución de llamada especifique el puntero de la vista a una lista de identificadores de elemento (PIDL). Solo se usa cuando se ha producir un error [**en IPersistIDList::SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) [**e IPersistFolder2::GetCurFolder.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pidl* \[ out\]
</dt> <dd>

Dirección del PIDL de la vista.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
