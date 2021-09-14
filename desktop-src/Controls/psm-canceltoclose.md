---
title: PSM_CANCELTOCLOSE mensaje (Prsht.h)
description: Enviado por una aplicación cuando ha realizado cambios desde la notificación APPLY de PSN \_ más reciente que no se puede cancelar. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ CancelToClose.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- PSM_CANCELTOCLOSE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167594"
---
# <a name="psm_canceltoclose-message"></a>Mensaje \_ CANCELTOCLOSE de PSM

Enviado por una aplicación cuando ha realizado cambios desde la notificación APPLY de [PSN \_ más](psn-apply.md) reciente que no se puede cancelar. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ CancelToClose.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose)

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

**PSM \_ CANCELTOCLOSE** deshabilita el botón **Cancelar** y cambia el texto **del** botón Aceptar a "Cerrar".

La mayoría de las hojas de propiedades esperan para realizar cambios irreversibles hasta que se recibe una \_ notificación APPLY de PSN. Sin embargo, en algunas circunstancias, una hoja de propiedades puede realizar cambios irreversibles fuera de la secuencia ESTÁNDAR DE PSN \_ APPLY/PSN \_ RESET. Un ejemplo es una hoja de propiedades que contiene un **botón Editar** que se usa para mostrar un cuadro de diálogo secundario para editar una propiedad. Cuando el usuario hace clic **en Aceptar** para enviar el cambio, la página de la hoja de propiedades tiene varias opciones.

-   Puede registrar los cambios, pero esperar hasta que reciba una notificación \_ PSN APPLY para aplicarlos. Este es el método preferido.
-   Puede aplicar los cambios inmediatamente después de salir del cuadro de diálogo secundario, pero recordar la configuración original. Esta configuración se puede usar para restaurar el estado original si se recibe una notificación \_ de RESTABLECIMIENTO de PSN.
-   Puede aplicar los cambios inmediatamente y no intentar restaurar la configuración original cuando recibe una notificación [de RESTABLECIMIENTO \_ de PSN.](psn-reset.md) Este enfoque no se recomienda, pero puede ser necesario si los cambios son demasiado largos para que las otras dos opciones sean prácticas.

Para la tercera opción, las aplicaciones deben enviar un **mensaje \_ CANCELTOCLOSE de PSM** a la hoja de propiedades. Indica al usuario que los cambios realizados con el cuadro de diálogo secundario no se pueden invertir haciendo clic en **el botón** Cancelar.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





