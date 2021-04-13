---
title: Código de notificación de CBEN_ENDEDIT (commctrl. h)
description: Se envía cuando el usuario ha finalizado una operación en el cuadro de edición o ha seleccionado un elemento de la lista desplegable del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421951"
---
# <a name="cben_endedit-notification-code"></a>Código de notificación de CBEN \_ ENDEDIT

Se envía cuando el usuario ha finalizado una operación en el cuadro de edición o ha seleccionado un elemento de la lista desplegable del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) que contiene información sobre cómo el usuario ha concluido la operación de edición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**False** para aceptar el código de notificación y permitir que el control muestre el elemento seleccionado; en caso contrario, **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CBEN \_ ENDEDITW** (Unicode) y **CBEN \_ ENDEDITA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca de los controles ComboBoxEx](comboboxex-controls.md)
</dt> </dl>

 

 





