---
title: PSM_GETRESULT mensaje (Prsht.h)
description: Las hojas de propiedades modeless usan para recuperar la información devuelta a las hojas de propiedades modales por PropertySheet. Puede enviar este mensaje explícitamente o usar la \_ macro GetResult de PropSheet.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167574"
---
# <a name="psm_getresult-message"></a>Mensaje \_ GETRESULT de PSM

Usado por hojas de propiedades modeless para recuperar la información devuelta a las hojas de propiedades modales [**por PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). Puede enviar este mensaje explícitamente o usar la macro [**\_ GetResult de PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult)

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

Devuelve un valor positivo si se realiza correctamente o -1 en caso contrario. Los siguientes valores devueltos tienen un significado especial.



| Código devuelto                                                                                         | Descripción                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ID \_ PSREBOOTSYSTEM**</dt> </dl>   | Una página envió un [**mensaje PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) a la hoja de propiedades. El equipo debe reiniciarse para que los cambios del usuario suban efecto.<br/> |
| <dl> <dt>**ID \_ PSRESTARTWINDOWS**</dt> </dl> | Una página envió un [**mensaje PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) a la hoja de propiedades. Windows debe reiniciarse para que los cambios del usuario suban efecto.<br/>  |



 

## <a name="remarks"></a>Observaciones

Para recuperar información de error extendida, llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

El valor devuelto para este mensaje es idéntico al que [**propertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelve para una hoja de propiedades modal.

[Versión 5.80.](common-control-versions.md) El [**valor devuelto PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) contiene información diferente para las hojas de propiedades modales y modeless. En algunos casos, las hojas de propiedades modeless pueden necesitar la información que hubieran recibido de **PropertySheet** si hubieran sido modales. En concreto, es posible que deban saber si se habría devuelto el \_ id. PSREBOOTSYSTEM o el identificador \_ PSRESTARTWINDOWS.

Para una hoja de propiedades modeless, el bucle de mensajes debe usar [**PSM \_ ISDIALOGMESSAGE para**](psm-isdialogmessage.md) pasar mensajes al cuadro de diálogo de hoja de propiedades y [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) para determinar cuándo destruir el cuadro de diálogo. Cuando el usuario hace clic en el **botón Aceptar** o **Cancelar,** **PSM \_ GETCURRENTPAGEHWND** devuelve **NULL.** A continuación, puede recuperar el valor que una hoja de propiedades modal habría recibido de [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) mediante el envío de **un mensaje \_ GETRESULT de PSM.**

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

