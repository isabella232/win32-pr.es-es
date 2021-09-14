---
title: PSM_GETCURRENTPAGEHWND mensaje (Prsht.h)
description: Recupera un identificador en la ventana de la página actual de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro \_ PropSheet GetCurrentPageHwnd.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- PSM_GETCURRENTPAGEHWND controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167577"
---
# <a name="psm_getcurrentpagehwnd-message"></a>Mensaje \_ GETCURRENTPAGEHWND de PSM

Recupera un identificador en la ventana de la página actual de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet GetCurrentPageHwnd.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador a la ventana de la página de hoja de propiedades actual.

## <a name="remarks"></a>Observaciones

Use el **mensaje PSM \_ GETCURRENTPAGEHWND** con hojas de propiedades modeless para determinar cuándo destruir el cuadro de diálogo. Cuando el usuario  hace  clic en el botón Aceptar o Cancelar, **PSM \_ GETCURRENTPAGEHWND** devuelve **NULL** y, a continuación, puede usar la [**función DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir el cuadro de diálogo.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

