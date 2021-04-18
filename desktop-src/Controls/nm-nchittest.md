---
title: Código de notificación de NM_NCHITTEST (commctrl. h)
description: Lo envía un control Rebar cuando el control recibe un mensaje de NCHITTEST de WM \_ . Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST controles de código de notificación de Windows
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
ms.openlocfilehash: f8af39fd792ecb9aeb463957f49f5722737e6ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658211"
---
# <a name="nm_nchittest-notification-code"></a>Código de notificación de NM \_ NCHITTEST

Lo envía un control Rebar cuando el control recibe un mensaje de [**\_ NCHITTEST de WM**](/windows/desktop/inputdev/wm-nchittest) . Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre el código de notificación. El miembro *PT* contiene las coordenadas del mouse del mensaje de la prueba de posicionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

A menos que se especifique lo contrario, devuelva cero para permitir que el control realice el procesamiento predeterminado del mensaje de la prueba de posicionamiento, o bien devuelva uno de los valores de HT \* documentados en [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para invalidar el procesamiento predeterminado de la prueba de posicionamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

