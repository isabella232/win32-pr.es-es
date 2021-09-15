---
description: Establece la posición de un elemento en la vista Shell. Usado por shshellfolderview \_ message.
title: SFVM_SETITEMPOS mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468112"
---
# <a name="sfvm_setitempos-message"></a>Mensaje \_ SETITEMPOS de SFVM

Establece la posición de un elemento en la vista Shell. Usado por [**el mensaje SHShellFolderView \_**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sip* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ SETITEMPOS de SFV.**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP1 \[\]<br/>                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




