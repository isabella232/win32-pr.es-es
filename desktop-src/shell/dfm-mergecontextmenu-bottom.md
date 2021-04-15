---
description: Permite que la devolución de llamada agregue elementos a la parte inferior del menú extendido.
title: Mensaje de DFM_MERGECONTEXTMENU_BOTTOM (ShlObj. h)
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
ms.openlocfilehash: b9274a36f531e53f86d05adab20b4970ea5ace84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984302"
---
# <a name="dfm_mergecontextmenu_bottom-message"></a>DFM \_ mensaje de MERGECONTEXTMENU \_ inferior

Permite que la devolución de llamada agregue elementos a la parte inferior del menú extendido.


```C++
DFM_MERGECONTEXTMENU_BOTTOM

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pqcminfo* \[ de\]
</dt> <dd>

Puntero a una estructura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contiene la información utilizada en la combinación.

</dd> <dt>

*uFlags* \[ de\]
</dt> <dd>

Marcas que especifican cómo se puede cambiar el menú contextual. Este parámetro usa los \_ \* valores CMF descritos en [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si los elementos se agregan al menú contextual extendido, deben ser compatibles con rutinas que respondan correctamente cuando se invoque uno de esos elementos mediante [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md).

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se construya el objeto de menú contextual predeterminado. Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada. Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 




