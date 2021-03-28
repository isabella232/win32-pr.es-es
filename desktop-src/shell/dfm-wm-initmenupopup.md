---
description: Se envía cuando un menú desplegable o un submenú está a punto de activarse. Esto permite que una aplicación modifique el menú antes de que se muestre, sin cambiar todo el menú.
title: Mensaje de DFM_WM_INITMENUPOPUP (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1c89731bdffc0e7d902e6c83b9a4f208134b7cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153913"
---
# <a name="dfm_wm_initmenupopup-message"></a>DFM \_ WM \_ INITMENUPOPUP Message

Se envía cuando un menú desplegable o un submenú está a punto de activarse. Esto permite que una aplicación modifique el menú antes de que se muestre, sin cambiar todo el menú.


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Identificador del menú desplegable o submenú.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

La palabra de orden inferior especifica la posición relativa de base cero del elemento de menú que abre el menú desplegable o submenú.

La palabra de orden superior indica si el menú desplegable es el menú ventana. Si el menú es el menú ventana, este parámetro es **true**; de lo contrario, es **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 




