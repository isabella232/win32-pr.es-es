---
description: Notifica al objeto de devolución de llamada que el usuario ha invocado uno de sus comandos de barra de herramientas o menú. Usado por IShellFolderViewCB::MessageSFVCB.
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: SFVM_INVOKECOMMAND mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256874"
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

## <a name="remarks"></a>Observaciones

Este mensaje sirve básicamente la misma función que un [**mensaje \_ WM COMMAND**](../menurc/wm-command.md) en un procedimiento de ventana convencional. Permite que el objeto de devolución de llamada controle cualquier elemento que haya agregado a la barra de menús o la herramienta Windows Explorer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
