---
title: PSM_SETCURSEL mensaje (Prsht.h)
description: Activa la página especificada en una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetCurSel.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- PSM_SETCURSEL controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167513"
---
# <a name="psm_setcursel-message"></a>Mensaje \_ SETCURSEL de PSM

Activa la página especificada en una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetCurSel.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la página. Una aplicación puede especificar el índice, el identificador o ambos. Si se especifican ambos, *lParam* tiene prioridad.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la página que se activará. Una aplicación puede especificar el índice, el identificador o ambos. Si se especifican ambos, *lParam* tiene prioridad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Observaciones

La ventana que pierde la activación recibe el código de notificación [ \_ KILLACTIVE](psn-killactive.md) de PSN y la ventana que obtiene la activación recibe el código de [notificación \_ SETACTIVE de PSN.](psn-setactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





