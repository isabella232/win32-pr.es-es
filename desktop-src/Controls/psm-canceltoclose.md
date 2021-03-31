---
title: Mensaje de PSM_CANCELTOCLOSE (Prsht. h)
description: Enviado por una aplicación cuando se han realizado cambios desde la notificación de aplicación de PSN más reciente \_ que no se puede cancelar. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ CancelToClose.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- PSM_CANCELTOCLOSE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150818"
---
# <a name="psm_canceltoclose-message"></a>Mensaje de PSM \_ CANCELTOCLOSE

Enviado por una aplicación cuando se han realizado cambios desde la notificación de [ \_ aplicación de PSN](psn-apply.md) más reciente que no se puede cancelar. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .

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

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

**PSM \_ CANCELTOCLOSE** deshabilita el botón **Cancelar** y cambia el texto del botón **Aceptar** a "cerrar".

La mayoría de las hojas de propiedades esperan a realizar cambios irreversibles hasta que \_ se recibe una notificación de aplicación de PSN. Sin embargo, en algunas circunstancias, una hoja de propiedades puede realizar cambios irreversibles fuera de la secuencia de restablecimiento de PSN estándar \_ Apply/PSN \_ . Un ejemplo es una hoja de propiedades que contiene un botón **Editar** que se utiliza para mostrar un cuadro de diálogo para editar una propiedad. Cuando el usuario hace clic en **Aceptar** para enviar el cambio, la página de la hoja de propiedades tiene varias opciones.

-   Puede registrar los cambios, pero espere hasta que reciba una notificación de \_ aplicación de PSN para aplicarlos. Este es el método preferido.
-   Puede aplicar los cambios inmediatamente después de salir del cuadro de diálogo, pero recuerde la configuración original. Esta configuración se puede usar para restaurar el estado original si \_ se recibe una notificación de restablecimiento de PSN.
-   Puede aplicar los cambios inmediatamente y no intentar restaurar la configuración original cuando recibe una notificación de [ \_ restablecimiento de PSN](psn-reset.md) . Este enfoque no se recomienda, pero puede ser necesario si los cambios son demasiado expuestos para que las otras dos opciones resulten prácticas.

En la tercera opción, las aplicaciones deben enviar un mensaje de **PSM \_ CANCELTOCLOSE** a la hoja de propiedades. Indica al usuario que no se pueden revertir los cambios realizados con el cuadro de diálogo haciendo clic en el botón **Cancelar** .

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





