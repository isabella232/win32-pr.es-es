---
title: Código de notificación de TBN_DRAGOUT (commctrl. h)
description: Se envía por un control de barra de herramientas cuando el usuario hace clic en un botón y, a continuación, mueve el cursor fuera del botón. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079119"
---
# <a name="tbn_dragout-notification-code"></a>Código de notificación de DRAGOUT de TBN \_

Se envía por un control de barra de herramientas cuando el usuario hace clic en un botón y, a continuación, mueve el cursor fuera del botón. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contiene información sobre este código de notificación. En este código de notificación, solo son válidos los miembros **HDR** y **iItem** de esta estructura. El miembro **iItem** de esta estructura contiene el identificador de comando del botón que se está arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Este código de notificación permite a una aplicación implementar la funcionalidad de arrastrar y colocar para los botones de la barra de herramientas. Al procesar este código de notificación, la aplicación iniciará la operación de arrastrar y colocar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





