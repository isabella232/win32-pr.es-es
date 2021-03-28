---
description: 'Permite que el objeto de devolución de llamada especifique los botones que se van a agregar a la barra de herramientas. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: Mensaje de SFVM_GETBUTTONS (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911398"
---
# <a name="sfvm_getbuttons-message"></a>SFVM \_ GETBUTTONS

Permite que el objeto de devolución de llamada especifique los botones que se van a agregar a la barra de herramientas. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*idCmdFirst \_ cbtnMax* \[\]
</dt> <dd>

Contiene los valores de 2 16 bits empaquetados en el parámetro con la macro [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) . La palabra de orden inferior contiene el identificador de comando inicial. La palabra de orden superior contiene el número de botones que se van a agregar, tal como se especifica en el mensaje [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) anterior.

</dd> <dt>

*pbtn* \[ enuncia\]
</dt> <dd>

La dirección de una matriz de estructuras [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) , una para cada botón que se va a agregar a la barra de herramientas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje está precedido por un mensaje [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) . El objeto de devolución de llamada debe controlar ese mensaje para especificar el número de botones y dónde se colocarán en la barra de herramientas. En función de cómo responda el objeto de devolución de llamada al mensaje **\_ GETBUTTONINFO de SFVM** , los botones especificados por el parámetro *pbtn* se anexarán o anteponerán a los botones estándar del objeto de vista de carpeta del sistema, o se reemplazarán al conjunto estándar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
