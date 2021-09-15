---
description: Notifica al objeto de devolución de llamada que se ha realizado un evento que afecta a uno de sus elementos. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_FSNOTIFY mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467179"
---
# <a name="sfvm_fsnotify-message"></a>Mensaje \_ FSNOTIFY de SFVM

Notifica al objeto de devolución de llamada que se ha realizado un evento que afecta a uno de sus elementos. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pppdl* \[ En\]
</dt> <dd>

Puntero del PIDL del elemento afectado.

</dd> <dt>

*lEvent* \[ En\]
</dt> <dd>

Valor SHCNE que indica qué evento se ha producido. Para obtener una lista de valores posibles, [**vea SHChangeNotify.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
