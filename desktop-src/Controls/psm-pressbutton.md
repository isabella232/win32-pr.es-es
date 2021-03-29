---
title: Mensaje de PSM_PRESSBUTTON (Prsht. h)
description: Simula la selección de un botón de la hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ PressButton.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- PSM_PRESSBUTTON controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493301"
---
# <a name="psm_pressbutton-message"></a>Mensaje de PSM \_ PRESSBUTTON

Simula la selección de un botón de la hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del botón que se va a seleccionar. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                            | Significado                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <dt>**PSBTN \_ APPLYNOW**</dt> </dl> | Selecciona el botón **aplicar** . Este valor no es válido cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <dt>**PSBTN \_ atrás**</dt> </dl>             | Selecciona el botón **atrás** .<br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <dt>**\_Cancelar PSBTN**</dt> </dl>       | Selecciona el botón **Cancelar** .<br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <dt>**\_Finalizar PSBTN**</dt> </dl>       | Selecciona el botón **Finalizar** .<br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <dt>**ayuda de PSBTN \_**</dt> </dl>             | Selecciona el botón **ayuda** . Este valor no es válido cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <dt>**PSBTN \_ siguiente**</dt> </dl>             | Selecciona el botón **siguiente** .<br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <dt>**PSBTN \_ Aceptar**</dt> </dl>                   | Selecciona el botón **Aceptar** . Este valor no es válido cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/>    |



 

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





