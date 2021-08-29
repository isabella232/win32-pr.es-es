---
description: SFVM \_ DIDDRAGDROP puede modificarse o no estar disponible.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: SFVM_DIDDRAGDROP mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34a7c129a5c80979ca9cf52fbbd73f05ce14cd5c074485c83110314435cbecf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009065"
---
# <a name="sfvm_diddragdrop-message"></a>Mensaje \_ DIDDRAGDROP de SFVM

\[**SFVM \_ DIDDRAGDROP** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Notifica a la función de devolución de llamada que ha comenzado una operación de arrastrar y colocar. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwEffect* \[ En\]
</dt> <dd>

Especificador de efecto de colocación de la [**enumeración DROPEFFECT.**](../com/dropeffect-constants.md) Esto se obtiene mediante una llamada a [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).

</dd> <dt>

*pIdo* \[ En\]
</dt> <dd>

Puntero a la [**instancia de IDataObject.**](/windows/win32/api/objidl/nn-objidl-idataobject)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
