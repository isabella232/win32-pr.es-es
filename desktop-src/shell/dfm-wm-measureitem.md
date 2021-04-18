---
description: Se envía a la ventana propietaria de un control o un elemento de menú cuando se crea el control o el menú.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Mensaje de DFM_WM_MEASUREITEM (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423704"
---
# <a name="dfm_wm_measureitem-message"></a>DFM \_ WM \_ MEASUREITEM Message

Se envía a la ventana propietaria de un control o un elemento de menú cuando se crea el control o el menú.


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

El valor del miembro **CtlID** de la estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) señalada por el parámetro *lpMeasureItem* . Este valor identifica el control que envió el mensaje **DFM de \_ \_ MEASUREITEM de WM** .

</dd> <dt>

*lpMeasureItem* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que contiene las dimensiones del elemento de menú o control dibujado por el propietario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando la ventana propietaria recibe el mensaje **DFM de \_ \_ MEASUREITEM WM** , el propietario rellena la estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) señalada por el parámetro *lpMeasureItem* del mensaje y devuelve; esto informa al sistema de las dimensiones del control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
