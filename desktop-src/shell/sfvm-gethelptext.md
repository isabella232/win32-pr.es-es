---
description: 'Permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda para los elementos de menú o los botones de la barra de herramientas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_GETHELPTEXT (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b33bd99c2dd1e6d1013da9015a5ff70bc111c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815478"
---
# <a name="sfvm_gethelptext-message"></a>SFVM \_ GETHELPTEXT

Permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda para los elementos de menú o los botones de la barra de herramientas. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTEXT 

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



 

 
