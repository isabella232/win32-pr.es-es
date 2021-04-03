---
title: Código de notificación de HDN_DROPDOWN (commctrl. h)
description: Lo envía un control de encabezado a su elemento primario cuando se hace clic en la flecha de cuadro desplegable del control de encabezado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905702"
---
# <a name="hdn_dropdown-notification-code"></a>\_Código de notificación de desplegable HDN

Lo envía un control de encabezado a su elemento primario cuando se hace clic en la flecha de cuadro desplegable del control de encabezado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En el ejemplo de la sección sintaxis se muestra cómo el receptor de notificaciones convierte **lParam** para recuperar la estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** contiene el identificador del control que envía este mensaje.

Este mensaje se envía solo si el estilo HDF \_ SPLITBUTTON está establecido en el elemento de encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





