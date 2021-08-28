---
title: TVN_SINGLEEXPAND de notificación (Commctrl.h)
description: Enviado por un control de vista de árbol con el estilo SINGLEEXPAND de TVS cuando el usuario abre o cierra un elemento de árbol con un solo \_ clic del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- TVN_SINGLEEXPAND de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61cd83dedbe16bad81c340f35a176b18804de6b7db6847fb65bc847160a2ff8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132205"
---
# <a name="tvn_singleexpand-notification-code"></a>Código de notificación DE TVN \_ SINGLEEXPAND

Enviado por un control de vista de árbol con el estilo [**\_ SINGLEEXPAND**](tree-view-control-window-styles.md) de TVS cuando el usuario abre o cierra un elemento de árbol con un solo clic del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve TVNRET \_ DEFAULT para permitir que se produzca el comportamiento predeterminado. Para modificar el comportamiento predeterminado, devuelva:



| Código devuelto                                                                                    | Descripción                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**TVNRET \_ SKIPOLD**</dt> </dl> | Omita el procesamiento predeterminado del elemento que no está seleccionado.<br/> |
| <dl> <dt>**TVNRET \_ SKIPNEW**</dt> </dl> | Omita el procesamiento predeterminado del elemento que se está seleccionando.<br/>   |



 

## <a name="remarks"></a>Comentarios

Para omitir el procesamiento predeterminado de los elementos seleccionados y no seleccionados, devuelva TVNRET \_ SKIPOLD y TVNRET SKIPNEW combinándolos con un \_ or lógico.

Este código de notificación solo se envía mediante controles de vista de árbol que tienen el estilo [**\_ SINGLEEXPAND de TVS.**](tree-view-control-window-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





