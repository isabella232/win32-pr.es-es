---
description: 'Permite que el objeto de devolución de llamada especifique una cadena de texto de información sobre herramientas para los elementos de menú o botones de barra de herramientas. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: Mensaje de SFVM_GETTOOLTIPTEXT (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffea70f6051ec435e14640ac70d2e9617b11305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002981"
---
# <a name="sfvm_gettooltiptext-message"></a>SFVM \_ GETTOOLTIPTEXT

Permite que el objeto de devolución de llamada especifique una cadena de texto de información sobre herramientas para los elementos de menú o botones de barra de herramientas. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*idCmd \_ cchMax* \[\]
</dt> <dd>

La palabra de orden inferior de este parámetro contiene el identificador de comando. La palabra de orden superior contiene el número de caracteres en el búfer de *miembros pszText* .

</dd> <dt>

*miembros pszText* \[ enuncia\]
</dt> <dd>

Una cadena terminada en null que contiene el texto de ayuda.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
