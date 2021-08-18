---
description: Notifica al objeto de devolución de llamada que el usuario ha invocado uno de sus comandos de barra de herramientas o menú. Usado por IShellFolderViewCB::MessageSFVCB.
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: SFVM_INVOKECOMMAND mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b33eba78e0680fe940569c7a7ccfb4a27c61c3ffcb6eead0f2ff6436ec74f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968654"
---
# <a name="sfvm_invokecommand-message"></a>Mensaje \_ INVOKECOMMAND de SFVM

Notifica al objeto de devolución de llamada que el usuario ha invocado uno de sus comandos de barra de herramientas o menú. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*idCmd* \[ en\]
</dt> <dd>

Identificador de comando de la barra de herramientas o el elemento de menú seleccionados.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este mensaje sirve básicamente la misma función que un [**mensaje \_ WM COMMAND**](../menurc/wm-command.md) en un procedimiento de ventana convencional. Permite que el objeto de devolución de llamada controle los elementos que ha agregado a la herramienta o barra de menús Windows Explorer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
