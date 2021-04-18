---
title: Mensaje de PSM_GETCURRENTPAGEHWND (Prsht. h)
description: Recupera un identificador de la ventana de la página actual de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ GetCurrentPageHwnd.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- PSM_GETCURRENTPAGEHWND controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658317"
---
# <a name="psm_getcurrentpagehwnd-message"></a>Mensaje de PSM \_ GETCURRENTPAGEHWND

Recupera un identificador de la ventana de la página actual de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .

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

Devuelve un identificador a la ventana de la página de la hoja de propiedades actual.

## <a name="remarks"></a>Observaciones

Use el mensaje **PSM \_ GETCURRENTPAGEHWND** con hojas de propiedades no modales para determinar cuándo se debe destruir el cuadro de diálogo. Cuando el usuario hace clic en el botón **Aceptar** o **Cancelar** , **PSM \_ GETCURRENTPAGEHWND** devuelve **null** y, a continuación, puede usar la función [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir el cuadro de diálogo.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

