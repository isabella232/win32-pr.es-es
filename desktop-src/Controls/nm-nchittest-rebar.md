---
title: Código de notificación de NM_NCHITTEST (rebar) (commctrl. h)
description: Lo envía un control Rebar cuando el control recibe un mensaje de NCHITTEST de WM \_ . Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- Código de notificación NM_NCHITTEST (rebar) controles de Windows
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb4568cad87017d9fff94deb60583ac0b4c1d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150758"
---
# <a name="nm_nchittest-rebar-notification-code"></a>Código de notificación de NM \_ NCHITTEST (rebar)

Lo envía un control Rebar cuando el control recibe un mensaje de [**\_ NCHITTEST de WM**](/windows/desktop/inputdev/wm-nchittest) . Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre el código de notificación. El miembro **dwItemSpec** contiene el índice de banda sobre el que se produjo el mensaje de la prueba de posicionamiento y el miembro **PT** contiene las coordenadas del mouse del mensaje de la prueba de posicionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva cero para permitir que el rebar realice el procesamiento predeterminado del mensaje de la prueba de posicionamiento, o bien devuelva uno de los valores de HT \* documentados en [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para invalidar el procesamiento predeterminado de la prueba de posicionamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

