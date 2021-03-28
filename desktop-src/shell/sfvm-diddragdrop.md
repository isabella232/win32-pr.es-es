---
description: SFVM \_ DIDDRAGDROP puede modificarse o no estar disponible.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: Mensaje de SFVM_DIDDRAGDROP (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997825"
---
# <a name="sfvm_diddragdrop-message"></a>SFVM \_ DIDDRAGDROP

\[**SFVM \_ DIDDRAGDROP** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Notifica a la función de devolución de llamada que se ha iniciado una operación de arrastrar y colocar. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwEffect* \[ de\]
</dt> <dd>

Un especificador de efecto de colocación de la enumeración [**DROPEFFECT**](../com/dropeffect-constants.md) . Esto se obtiene llamando a [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).

</dd> <dt>

*pIdo* \[ de\]
</dt> <dd>

Puntero a la instancia de [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
