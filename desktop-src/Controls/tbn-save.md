---
title: Código de notificación de TBN_SAVE (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de guardarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804003"
---
# <a name="tbn_save-notification-code"></a>TBN \_ Guardar código de notificación

Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de guardarse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La aplicación recibirá este código de notificación una vez al inicio del proceso de guardado y una vez para cada botón. Este código de notificación le ofrece la oportunidad de agregar su propia información a que haya guardado el shell. Si no desea agregar información, omita el código de notificación. Consulte [Personalización](toolbar-controls-overview.md) de la barra de herramientas para obtener una explicación más detallada de cómo controlar el almacenamiento de TBN \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[restauración de TBN \_](tbn-restore.md)
</dt> </dl>

 

 





