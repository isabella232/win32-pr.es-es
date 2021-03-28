---
description: 'Permite que la devolución de llamada modifique los valores de CFM \_ XXX pasados a IContextMenu:: QueryContextMenu.'
title: Mensaje de DFM_MODIFYQCMFLAGS (ShlObj. h)
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
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907727"
---
# <a name="dfm_modifyqcmflags-message"></a>DFM \_ MODIFYQCMFLAGS

Permite que la devolución de llamada modifique los valores de CFM \_ XXX pasados a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*puNewFlags* \[ de\]
</dt> <dd>

Puntero a los nuevos valores de marca.

</dd> <dt>

*uFlags* \[ de\]
</dt> <dd>

Marcas que especifican cómo se puede cambiar el menú contextual. Este parámetro usa los \_ valores de CMF XXX descritos en [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 




