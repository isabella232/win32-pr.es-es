---
description: Permite que el objeto de devolución de llamada modifique Windows menú emergente explorador antes de que se muestre. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_INITMENUPOPUP mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fd69d19f753c1c72c1e0c143a0aface2cdb234cb2ace8c87d559834b97bbf0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592325"
---
# <a name="sfvm_initmenupopup-message"></a>Mensaje \_ SFVM INITMENUPOPUP

Permite que el objeto de devolución de llamada modifique Windows menú emergente explorador antes de que se muestre. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*idCmd \_ nIndex* \[ en\]
</dt> <dd>

La palabra de orden bajo de este parámetro contiene el valor del primer identificador de comando reservado para los comandos de cliente. La palabra de orden superior contiene el índice del menú.

</dd> <dt>

*hmenu* \[ in, out\]
</dt> <dd>

Identificador del menú.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El objeto de vista de carpeta del sistema envía este mensaje cuando se selecciona un menú, pero antes de que se muestre. Procese este mensaje si, por ejemplo, necesita habilitar o deshabilitar los comandos de menú. El menú emergente puede ser:

-   Menú Archivo, Editar o Ver.
-   Menú de nivel superior definido por el cliente.
-   Submenú definido por el cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SFVM \_ MERGEMENU**](sfvm-mergemenu.md)
</dt> </dl>

 

 
