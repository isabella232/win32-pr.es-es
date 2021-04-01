---
title: Código de notificación de NM_CLICK (syslink) (commctrl. h)
description: Notifica a la ventana primaria de un control que el usuario ha haga clic en un hipervínculo con el botón primario del mouse en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e92d7c92-f2c6-44aa-bce5-3bb07c184e7d
keywords:
- Código de notificación de NM_CLICK (syslink), controles de Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea34682b0cfdfdf1206a133abe4fdb22b8af5cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151273"
---
# <a name="nm_click-syslink-notification-code"></a>NM \_ click (syslink) código de notificación

Notifica a la ventana primaria de un control que el usuario ha haga clic en un hipervínculo con el botón primario del mouse en el control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CLICK

    pnmLink = (PNMLINK) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink)
</dt> <dt>

[**\_notificaciones de WM**](wm-notify.md)
</dt> </dl>

 

 





