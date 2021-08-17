---
description: Notifica a IShellView cuando uno de sus objetos se coloca en el Portapapeles como resultado de un comando de menú. Lo usa shshellfolderview \_ message.
title: SFVM_SETCLIPBOARD mensaje (Shlobj.h)
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
ms.openlocfilehash: 99548be90c7f4fb9b840e4d4c6f816710c6e02cc1a888ce0c1c774f73c58f668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858217"
---
# <a name="sfvm_setclipboard-message"></a>Mensaje \_ SETCLIPBOARD de SFVM

Notifica a [**IShellView cuando**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) uno de sus objetos se coloca en el Portapapeles como resultado de un comando de menú. Usado por [**el mensaje SHShellFolderView \_**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwEffect* \[ En\]
</dt> <dd>

Use (WPARAM)-2 si el elemento se está cortando al Portapapeles o (WPARAM)-3 si el elemento se copia en el Portapapeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




