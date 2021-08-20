---
description: Permite que la devolución de llamada modifique los valores XXX de CFM pasados \_ a IContextMenu::QueryContextMenu.
title: DFM_MODIFYQCMFLAGS mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 62ce86426b31abfb6dec67d7ee45b01a8bc47ba10c40ce9ed00051dd414a0ffd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223595"
---
# <a name="dfm_modifyqcmflags-message"></a>Mensaje \_ MODIFYQCMFLAGS de DFM

Permite que la devolución de llamada modifique los valores XXX de CFM \_ pasados [**a IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*puNewFlags* \[ En\]
</dt> <dd>

Puntero a los nuevos valores de marca.

</dd> <dt>

*uFlags* \[ En\]
</dt> <dd>

Marcas que especifican cómo se puede cambiar el menú contextual. Este parámetro usa los valores XXX de CMF \_ descritos [**en IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                             |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




