---
description: Permite que la devolución de llamada agregue elementos a la parte inferior del menú extendido.
title: DFM_MERGECONTEXTMENU_BOTTOM mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 37414335-4f3c-461e-bd05-d6ef850f972a
api_name:
- DFM_MERGECONTEXTMENU_BOTTOM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11dade0f4b9526fa3c384f612b2c23eb77b437ef361d16c2adffc0a49df2ca28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111845"
---
# <a name="dfm_mergecontextmenu_bottom-message"></a>Mensaje \_ MERGECONTEXTMENU BOTTOM de DFM \_

Permite que la devolución de llamada agregue elementos a la parte inferior del menú extendido.


```C++
DFM_MERGECONTEXTMENU_BOTTOM

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pqcminfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contiene la información utilizada en la combinación.

</dd> <dt>

*uFlags* \[ En\]
</dt> <dd>

Marcas que especifican cómo se puede cambiar el menú contextual. Este parámetro usa los valores de CMF \_ \* descritos en [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si los elementos se agregan al menú contextual extendido, deben ser compatibles con rutinas que respondan correctamente cuando se invoca uno de esos elementos mediante [**\_ INVOKECOMMAND de DFM.**](dfm-invokecommand.md)

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada en función de cómo se construya el objeto de menú contextual predeterminado. Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)y [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX es**](dfm-invokecommandex.md) una versión extendida de este mensaje y proporciona más información a la devolución de llamada. Use **DFM \_ INVOKECOMMANDEX si** la información adicional proporcionada por esa interfaz es necesaria en la implementación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




