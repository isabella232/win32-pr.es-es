---
description: Se envía a la ventana de propietario de un control o elemento de menú cuando se crea el control o el menú.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: DFM_WM_MEASUREITEM mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e7ad0d39a56f598a8ef4773c70f4f438388e91a2154b3083fdf85a1ebebec22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860903"
---
# <a name="dfm_wm_measureitem-message"></a>Mensaje \_ MEASUREITEM de WM DE DFM \_

Se envía a la ventana de propietario de un control o elemento de menú cuando se crea el control o el menú.


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Valor del miembro **CtlID** de la [**estructura MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a la que apunta el *parámetro lpMeasureItem.* Este valor identifica el control que envió el mensaje **\_ \_ MEASUREITEM de WM DE DFM.**

</dd> <dt>

*lpMeasureItem* \[ out\]
</dt> <dd>

Puntero a una [**estructura MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que contiene las dimensiones del elemento de menú o control dibujado por el propietario.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando la ventana de propietario recibe el mensaje **\_ \_ MEASUREITEM de DFM WM,** el propietario rellena la estructura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a la que apunta el parámetro *lpMeasureItem* del mensaje y devuelve ; esto informa al sistema de las dimensiones del control.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
