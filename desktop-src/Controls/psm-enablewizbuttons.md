---
title: PSM_ENABLEWIZBUTTONS mensaje (Prsht.h)
description: Habilita o deshabilita cualquiera de los botones estándar en un asistente de Aero. Puede enviar este mensaje explícitamente o usar la macro PropSheet \_ EnableWizButtons.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- PSM_ENABLEWIZBUTTONS controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167581"
---
# <a name="psm_enablewizbuttons-message"></a>Mensaje \_ ENABLEWIZBUTTONS de PSM

Habilita o deshabilita cualquiera de los botones estándar en un asistente de Aero. Puede enviar este mensaje explícitamente o usar la macro [**PropSheet \_ EnableWizButtons.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o varios de los valores siguientes que especifican qué botones de hoja de propiedades se van a habilitar. Si se incluye un valor de botón en este parámetro y *en lParam,* se habilita.



| Value                                                                                                                                                                                 | Significado                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIWI \_ BACK**</dt> </dl>                               | Botón  Atrás.<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIWI \_ CANCEL**</dt> </dl>                         | Botón **Cancelar.**<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIWIWI \_ DISABLEDFINISH**</dt> </dl> | Botón **Finalizar.**<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIWI \_ FINISH**</dt> </dl>                         | Botón **Finalizar.**<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIWI \_ NEXT**</dt> </dl>                               | Botón  Siguiente.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uno o varios de los mismos valores usados en *wParam*, especificando qué botones se ven afectados por esta llamada. Si aparece un valor de botón en este parámetro pero no en *wParam*, indica que el botón debe deshabilitarse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





