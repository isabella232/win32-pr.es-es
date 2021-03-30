---
title: Código de notificación de CBEN_DRAGBEGIN (commctrl. h)
description: Se envía cuando el usuario comienza a arrastrar la imagen del elemento mostrado en la parte de edición del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150978"
---
# <a name="cben_dragbegin-notification-code"></a>Código de notificación de DRAGBEGIN de CBEN \_

Se envía cuando el usuario comienza a arrastrar la imagen del elemento mostrado en la parte de edición del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Si la aplicación receptora implementa la funcionalidad de arrastrar y colocar del control, la aplicación comenzará la operación de arrastrar y colocar en respuesta a este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CBEN \_ DRAGBEGINW** (Unicode) y **CBEN \_ DRAGBEGINA** (ANSI)<br/>             |



 

 





