---
title: Mensaje de PSM_ENABLEWIZBUTTONS (Prsht. h)
description: Habilita o deshabilita cualquiera de los botones estándar en un asistente de Aero. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet EnableWizButtons.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- PSM_ENABLEWIZBUTTONS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996642"
---
# <a name="psm_enablewizbuttons-message"></a>Mensaje de PSM \_ ENABLEWIZBUTTONS

Habilita o deshabilita cualquiera de los botones estándar en un asistente de Aero. Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o varios de los siguientes valores que especifican qué botones de la hoja de propiedades se van a habilitar. Si un valor de botón está incluido en este parámetro y *lParam*, se habilita.



| Value                                                                                                                                                                                 | Significado                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ atrás**</dt> </dl>                               | Botón **atrás** .<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**\_Cancelar PSWIZB**</dt> </dl>                         | Botón **Cancelar** .<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | El botón **Finalizar** .<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**\_Finalizar PSWIZB**</dt> </dl>                         | El botón **Finalizar** .<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ siguiente**</dt> </dl>                               | Botón **siguiente** .<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uno o varios de los mismos valores utilizados en *wParam*, que especifican qué botones se ven afectados por esta llamada. Si aparece un valor de botón en este parámetro pero no en *wParam*, indica que se debe deshabilitar el botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





