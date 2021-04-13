---
title: Mensaje de PSM_GETRESULT (Prsht. h)
description: Lo usan las hojas de propiedades no modales para recuperar la información devuelta a las hojas de propiedades modales por hoja. Puede enviar este mensaje explícitamente o usar la \_ macro PropSheet GetResult.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534917"
---
# <a name="psm_getresult-message"></a>Mensaje de PSM \_ GETRESULT

Lo usan las hojas de propiedades no modales para recuperar la información devuelta a las hojas de propiedades modales por [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). Puede enviar este mensaje explícitamente o usar la macro [**PropSheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .

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

Devuelve un valor positivo si es correcto, o-1 en caso contrario. Los siguientes valores devueltos tienen un significado especial.



| Código devuelto                                                                                         | Descripción                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ID \_ PSREBOOTSYSTEM**</dt> </dl>   | Una página envió un mensaje de [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) a la hoja de propiedades. El equipo debe reiniciarse para que los cambios del usuario surtan efecto.<br/> |
| <dl> <dt>**ID \_ PSRESTARTWINDOWS**</dt> </dl> | Una página envió un mensaje de [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) a la hoja de propiedades. Windows debe reiniciarse para que los cambios del usuario surtan efecto.<br/>  |



 

## <a name="remarks"></a>Observaciones

Para recuperar la información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

El valor devuelto para este mensaje es idéntico al que devuelve [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) para una hoja de propiedades modal.

[Versión 5,80.](common-control-versions.md) El valor devuelto de [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) incluye información diferente para las hojas de propiedades modales y no modales. En algunos casos, las hojas de propiedades no modales pueden necesitar la información que habrían recibido de **hoja** si hubieran sido modales. En concreto, es posible que necesite saber si se habrían \_ devuelto el identificador PSREBOOTSYSTEM o ID \_ PSRESTARTWINDOWS.

En una hoja de propiedades no modal, el bucle de mensajes debe usar [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) para pasar mensajes al cuadro de diálogo de la hoja de propiedades y [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) para determinar cuándo se debe destruir el cuadro de diálogo. Cuando el usuario hace clic en el botón **Aceptar** o **Cancelar** , **PSM \_ GETCURRENTPAGEHWND** devuelve **null**. Después, puede recuperar el valor que una hoja de propiedades modal habría recibido de [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) mediante el envío de un mensaje de **PSM \_ GETRESULT** .

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

