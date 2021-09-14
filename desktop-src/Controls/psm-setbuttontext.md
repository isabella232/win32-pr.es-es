---
title: PSM_SETBUTTONTEXT mensaje (Prsht.h)
description: Establece el texto de un botón en un asistente de Avión. Puede enviar este mensaje explícitamente o mediante la macro \_ SetButtonText de PropSheet.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- PSM_SETBUTTONTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167514"
---
# <a name="psm_setbuttontext-message"></a>Mensaje \_ SETBUTTONTEXT de PSM

Establece el texto de un botón en un asistente de Avión. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetButtonText de PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uno de los siguientes valores que especifica el botón cuyo texto se establece.



| Value                                                                                                                                                                                 | Significado                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIWI \_ BACK**</dt> </dl>                               | Botón  Atrás.<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIWI \_ CANCEL**</dt> </dl>                         | Botón **Cancelar.**<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIWI \_ DISABLEDFINISH**</dt> </dl> | Botón **Finalizar.**<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIWI \_ FINISH**</dt> </dl>                         | Botón **Finalizar.**<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIWI \_ NEXT**</dt> </dl>                               | Botón  Siguiente.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Texto que se establecerá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **PSM \_ SETBUTTONTEXTW** (Unicode)<br/>                                       |



 

 





