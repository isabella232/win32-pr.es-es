---
title: Mensaje de PSM_SETCURSEL (Prsht. h)
description: Activa la página especificada en una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetCurSel.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- PSM_SETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150188"
---
# <a name="psm_setcursel-message"></a>Mensaje de PSM \_ SETCURSEL

Activa la página especificada en una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la página. Una aplicación puede especificar el índice o el identificador o ambos. Si se especifican ambos, *lParam* tiene prioridad.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la página que se va a activar. Una aplicación puede especificar el índice o el identificador o ambos. Si se especifican ambos, *lParam* tiene prioridad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La ventana que está perdiendo la activación recibe el código de notificación [PSN \_ KILLACTIVE](psn-killactive.md) y la ventana que obtiene la activación recibe el código de notificación [PSN \_ SETACTIVE](psn-setactive.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





