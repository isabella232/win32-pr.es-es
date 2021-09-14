---
title: CBEN_ENDEDIT de notificación (Commctrl.h)
description: Se envía cuando el usuario ha finalizado una operación dentro del cuadro de edición o ha seleccionado un elemento de la lista desplegable del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT código de notificación Windows controles
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173906"
---
# <a name="cben_endedit-notification-code"></a>Código de notificación ENDEDIT de CBEN \_

Se envía cuando el usuario ha finalizado una operación dentro del cuadro de edición o ha seleccionado un elemento de la lista desplegable del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) que contiene información sobre cómo el usuario finalizó la operación de edición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**FALSE** para aceptar el código de notificación y permitir que el control muestre el elemento seleccionado; de lo contrario, **TRUE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CBEN \_ ENDEDITW** (Unicode) y **CBEN \_ ENDEDITA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca de los controles ComboBoxEx](comboboxex-controls.md)
</dt> </dl>

 

 





