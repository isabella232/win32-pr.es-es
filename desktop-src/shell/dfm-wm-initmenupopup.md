---
description: 'DFM_WM_INITMENUPOPUP mensaje: se envía cuando un menú desplegable o submenú está a punto de activarse. Esto permite a una aplicación modificar el menú antes de que se muestre, sin cambiar todo el menú.'
title: DFM_WM_INITMENUPOPUP mensaje (Shlobj.h)
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
ms.openlocfilehash: 4cb68b8251fa383ae9386eae3e6753158330c4be7566f02a8758a72dfe05de03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943155"
---
# <a name="dfm_wm_initmenupopup-message"></a>Mensaje \_ INITMENUPOPUP de DFM WM \_

Se envía cuando un menú desplegable o submenú está a punto de activarse. Esto permite a una aplicación modificar el menú antes de que se muestre, sin cambiar todo el menú.


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Identificador del menú desplegable o submenú.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

La palabra de orden bajo especifica la posición relativa de base cero del elemento de menú que abre el menú desplegable o submenú.

La palabra de orden superior indica si el menú desplegable es el menú de la ventana. Si el menú es el menú de la ventana, este parámetro es **TRUE**; de lo contrario, es **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




