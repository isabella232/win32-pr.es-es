---
description: 'Notifica al objeto de devolución de llamada que el usuario ha invocado uno de sus comandos de menú o barra de herramientas. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: Mensaje de SFVM_INVOKECOMMAND (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913313"
---
# <a name="sfvm_invokecommand-message"></a>SFVM \_ INVOKECOMMAND

Notifica al objeto de devolución de llamada que el usuario ha invocado uno de sus comandos de menú o barra de herramientas. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*idCmd* \[ en\]
</dt> <dd>

IDENTIFICADOR de comando de la barra de herramientas o el elemento de menú seleccionado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje sirve esencialmente la misma función que un mensaje de [**\_ comando de WM**](../menurc/wm-command.md) en un procedimiento de ventana convencional. Permite que el objeto de devolución de llamada controle los elementos que ha agregado a la herramienta explorador de Windows o a la barra de menús.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
