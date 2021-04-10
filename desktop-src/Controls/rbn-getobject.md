---
title: Código de notificación de RBN_GETOBJECT (commctrl. h)
description: Enviado por un control rebar creado con el \_ estilo REGISTERDROP de RBS cuando se arrastra un objeto sobre una banda en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- RBN_GETOBJECT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150651"
---
# <a name="rbn_getobject-notification-code"></a>RBN \_ código de notificación GETOBJECT

Enviado por un control rebar creado con el [**estilo \_ REGISTERDROP de RBS**](rebar-control-styles.md) cuando se arrastra un objeto sobre una banda en el control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contiene información sobre la banda sobre la que se arrastra el objeto y también recibe los datos proporcionados por la aplicación receptora en respuesta a este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto para este código de notificación debe ser cero.

## <a name="remarks"></a>Observaciones

Para recibir el \_ código de notificación GETOBJECT de RBN, INICIALICE OLE con una llamada a [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) o [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

