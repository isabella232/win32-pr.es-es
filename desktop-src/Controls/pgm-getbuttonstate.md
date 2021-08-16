---
title: PGM_GETBUTTONSTATE mensaje (Commctrl.h)
description: Recupera el estado del botón especificado en un control de paginación. Puede enviar este mensaje explícitamente o usar la macro Pager \_ GetButtonState.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- PGM_GETBUTTONSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2014b6e36a0ab883155d786760ef54f02c89ee0d17192d6082d40ad19eec95a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830196"
---
# <a name="pgm_getbuttonstate-message"></a>Mensaje \_ GETBUTTONSTATE de PGM

Recupera el estado del botón especificado en un control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ GetButtonState.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Indica para qué botón se va a recuperar el estado. Puede ser uno de los siguientes valores:



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <dt>**PGB \_ TOPORLEFT**</dt> </dl>             | Indica el botón superior de un control de paginación [**\_ PGS VERT**](pager-control-styles.md) o el botón izquierdo de un control de paginación [**\_ HORZ de PGS.**](pager-control-styles.md) <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <dt>**PGB \_ BOTTOMORRIGHT**</dt> </dl> | Indica el botón inferior de un control de paginación [**\_ PGS VERT**](pager-control-styles.md) o el botón derecho en un control de paginación [**\_ HORZ de PGS.**](pager-control-styles.md) <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el estado del botón especificado en *lParam*. Este será uno o varios de los siguientes valores (si se devuelve más de un valor, se combinarán mediante un OR bit a bit):



| Código devuelto                                                                                   | Descripción                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**PGF \_ INVISIBLE**</dt> </dl> | El botón no está visible. <br/>      |
| <dl> <dt>**PGF \_ NORMAL**</dt> </dl>    | El botón está en estado normal. <br/>  |
| <dl> <dt>**PGF \_ ATENUADO**</dt> </dl>    | El botón está en estado atenuado. <br/>  |
| <dl> <dt>**PGF \_ DEPRESSED**</dt> </dl> | El botón está presionado. <br/> |
| <dl> <dt>**PGF \_ HOT**</dt> </dl>       | El botón está en estado "hot". <br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





