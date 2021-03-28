---
description: 'Notifica al objeto de devolución de llamada que se está creando la ventana vista de carpetas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_WINDOWCREATED (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d545feadecdaadbf776f94e653df8b71150ac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986094"
---
# <a name="sfvm_windowcreated-message"></a>SFVM \_ WINDOWCREATED

Notifica al objeto de devolución de llamada que se está creando la ventana vista de carpetas. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndView* \[ de\]
</dt> <dd>

Identificador de la ventana de la vista de carpetas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
