---
title: Mensaje de PGM_GETBUTTONSTATE (commctrl. h)
description: Recupera el estado del botón especificado en un control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro GetButtonState de buscapersonas \_ .
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- PGM_GETBUTTONSTATE controles de mensajes de Windows
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
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996731"
---
# <a name="pgm_getbuttonstate-message"></a>\_Mensaje GETBUTTONSTATE PGM

Recupera el estado del botón especificado en un control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetButtonState de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Indica el botón para el que se va a recuperar el estado. Puede ser uno de los siguientes valores:



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <dt>**PGB \_ TOPORLEFT**</dt> </dl>             | Indica el botón superior de un control de paginación de [**págs \_ Vert**](pager-control-styles.md) o el botón izquierdo de un control de paginación de [**págs \_ horizontal**](pager-control-styles.md) . <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <dt>**PGB \_ BOTTOMORRIGHT**</dt> </dl> | Indica el botón inferior de un control de paginación de [**págs \_ Vert**](pager-control-styles.md) o el botón secundario en un control de paginación de [**págs \_ horizontal**](pager-control-styles.md) . <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el estado del botón especificado en *lParam*. Este será uno o varios de los valores siguientes (si más se devuelve un valor, se combinarán mediante una operación OR bit a bit):



| Código devuelto                                                                                   | Descripción                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**PGF \_ invisible**</dt> </dl> | El botón no está visible. <br/>      |
| <dl> <dt>**PGF \_ normal**</dt> </dl>    | El botón está en estado normal. <br/>  |
| <dl> <dt>**PGF \_ atenuado**</dt> </dl>    | El botón está en estado atenuado. <br/>  |
| <dl> <dt>**PGF \_ presionado**</dt> </dl> | El botón está en estado presionado. <br/> |
| <dl> <dt>**PGF en \_ caliente**</dt> </dl>       | El botón está en estado activo. <br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





