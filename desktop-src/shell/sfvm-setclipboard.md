---
description: Notifica a IShellView cuando uno de sus objetos se coloca en el portapapeles como resultado de un comando de menú. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_SETCLIPBOARD (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997945"
---
# <a name="sfvm_setclipboard-message"></a>\_Mensaje SETCLIPBOARD SFVM

Notifica a [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) cuando uno de sus objetos se coloca en el portapapeles como resultado de un comando de menú. Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwEffect* \[ de\]
</dt> <dd>

Use (WPARAM)-2 Si el elemento se está cortando en el portapapeles o (WPARAM)-3 si el elemento se va a copiar en el portapapeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 




