---
title: PSM_PRESSBUTTON mensaje (Prsht.h)
description: Simula la selección de un botón de hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro \_ PressButton de PropSheet.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- PSM_PRESSBUTTON controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167534"
---
# <a name="psm_pressbutton-message"></a>Mensaje \_ PRESSBUTTON de PSM

Simula la selección de un botón de hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PressButton de PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del botón que se selecciona. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                            | Significado                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <dt>**PSBTN \_ APPLYNOW**</dt> </dl> | Selecciona el **botón** Aplicar. Este valor no es válido cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <dt>**PSBTN \_ BACK**</dt> </dl>             | Selecciona el **botón** Atrás.<br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <dt>**PSBTN \_ CANCEL**</dt> </dl>       | Selecciona el **botón** Cancelar.<br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <dt>**PSBTN \_ FINISH**</dt> </dl>       | Selecciona el **botón** Finalizar.<br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <dt>**AYUDA DE \_ PSBTN**</dt> </dl>             | Selecciona el botón **Ayuda.** Este valor no es válido cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <dt>**PSBTN \_ NEXT**</dt> </dl>             | Selecciona el **botón** Siguiente.<br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <dt>**PSBTN \_ OK**</dt> </dl>                   | Selecciona el **botón** Aceptar. Este valor no es válido cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





