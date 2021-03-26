---
description: 'Permite que el objeto de devolución de llamada modifique un menú emergente del explorador de Windows antes de que se muestre. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_INITMENUPOPUP (ShlObj. h)
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
ms.openlocfilehash: 1f9a2a169b232fe3ad16eeee8816536ed81c74dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986078"
---
# <a name="sfvm_initmenupopup-message"></a>SFVM \_ INITMENUPOPUP

Permite que el objeto de devolución de llamada modifique un menú emergente del explorador de Windows antes de que se muestre. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*idCmd \_ NINDEX* \[\]
</dt> <dd>

La palabra de orden inferior de este parámetro contiene el valor del primer identificador de comando reservado para los comandos del cliente. La palabra de orden superior contiene el índice del menú.

</dd> <dt>

*HMENU* \[ in, out\]
</dt> <dd>

Identificador del menú.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El objeto de vista de carpeta del sistema envía este mensaje cuando se selecciona un menú, pero antes de que se muestre. Procese este mensaje si, por ejemplo, necesita habilitar o deshabilitar comandos de menú. El menú emergente puede ser:

-   Menú Archivo, editar o ver.
-   Un menú de nivel superior definido por el cliente.
-   Un submenú definido por el cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SFVM \_ MERGEMENU**](sfvm-mergemenu.md)
</dt> </dl>

 

 
