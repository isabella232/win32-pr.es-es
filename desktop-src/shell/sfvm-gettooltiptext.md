---
description: Permite que el objeto de devolución de llamada especifique una cadena de texto de información sobre herramientas para los elementos de menú o los botones de la barra de herramientas. Usado por IShellFolderViewCB::MessageSFVCB.
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: SFVM_GETTOOLTIPTEXT mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3350d1f772cd78c97f7b57b47084c761808583dfe5396fafcdad336291a3a717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858227"
---
# <a name="sfvm_gettooltiptext-message"></a>Mensaje \_ GETTOOLTIPTEXT de SFVM

Permite que el objeto de devolución de llamada especifique una cadena de texto de información sobre herramientas para los elementos de menú o los botones de la barra de herramientas. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*idCmd \_ cchMax* \[ en\]
</dt> <dd>

La palabra de orden bajo de este parámetro contiene el identificador del comando. La palabra de orden superior contiene el número de caracteres del búfer *pszText.*

</dd> <dt>

*pszText* \[ out\]
</dt> <dd>

Cadena terminada en NULL que contiene el texto de ayuda.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
