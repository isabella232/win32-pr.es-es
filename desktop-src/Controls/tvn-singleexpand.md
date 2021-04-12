---
title: Código de notificación de TVN_SINGLEEXPAND (commctrl. h)
description: Enviado por un control de vista de árbol con el \_ estilo de SINGLEEXPAND de los televisores cuando el usuario abre o cierra un elemento de árbol con un solo clic del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- TVN_SINGLEEXPAND controles de código de notificación de Windows
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
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489635"
---
# <a name="tvn_singleexpand-notification-code"></a>Código de notificación de SINGLEEXPAND de TVN \_

Enviado por un control de vista de árbol con el estilo de [**\_ SINGLEEXPAND de los televisores**](tree-view-control-window-styles.md) cuando el usuario abre o cierra un elemento de árbol con un solo clic del mouse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ el valor predeterminado de TVNRET para permitir que se produzca el comportamiento predeterminado. Para modificar el comportamiento predeterminado, devuelva:



| Código devuelto                                                                                    | Descripción                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**TVNRET \_ SKIPOLD**</dt> </dl> | Omitir el procesamiento predeterminado del elemento que se va a anular la selección.<br/> |
| <dl> <dt>**TVNRET \_ SKIPNEW**</dt> </dl> | Omitir el procesamiento predeterminado del elemento que se va a seleccionar.<br/>   |



 

## <a name="remarks"></a>Observaciones

Para omitir el procesamiento predeterminado de los elementos seleccionados y no seleccionados, devuelva TVNRET \_ SKIPOLD y TVNRET \_ SKIPNEW combinándolos con un operador lógico or.

Este código de notificación solo lo envían los controles de vista de árbol que tienen el estilo [**\_ SINGLEEXPAND de TV**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





