---
description: Permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda para los elementos de menú o los botones de la barra de herramientas. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_GETHELPTEXT mensaje (Shlobj.h)
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
ms.openlocfilehash: c015c1999cbd60174da1994d92766b4f334630294767ee390be21340aef97cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661025"
---
# <a name="sfvm_gethelptext-message"></a>Mensaje \_ GETHELPTEXT de SFVM

Permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda para los elementos de menú o los botones de la barra de herramientas. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTEXT 

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



 

 
