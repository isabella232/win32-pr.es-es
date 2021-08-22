---
description: Permite que la devolución de llamada agregue elementos al menú.
title: DFM_MERGECONTEXTMENU mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ddd071e40d3c017a513eb0e85efb634df530a8686afaf7df59b922602d37f22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455975"
---
# <a name="dfm_mergecontextmenu-message"></a>Mensaje \_ MERGECONTEXTMENU de DFM

Permite que la devolución de llamada agregue elementos al menú.


```C++
DFM_MERGECONTEXTMENU

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

## <a name="remarks"></a>Observaciones

Si los elementos se agregan al menú contextual, deben ser compatibles con rutinas que respondan correctamente cuando se invoca uno de esos elementos mediante [**\_ INVOKECOMMAND de DFM.**](dfm-invokecommand.md)

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada en función de cómo se implemente el objeto de menú contextual predeterminado. Hay dos API para su implementación, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)y [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX es**](dfm-invokecommandex.md) una versión extendida de este mensaje y proporciona más información a la devolución de llamada. Use **DFM \_ INVOKECOMMANDEX si** la información adicional proporcionada por esa interfaz es necesaria en la implementación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




