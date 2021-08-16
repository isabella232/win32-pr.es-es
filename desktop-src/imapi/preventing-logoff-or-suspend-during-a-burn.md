---
title: Evitar el cierre de sesión o suspender durante una grabación
description: Si no se toman las precauciones adecuadas dentro de una aplicación, es posible que un usuario cierre la sesión durante una operación de grabación. Esto conduce a la interrupción del proceso de grabación, lo que puede provocar la pérdida de datos y, posiblemente, hacer que el disco sea inutilizable.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f3dd6980db72854ff65d657cc58730335febcb1dbc8c4a467eedead88f5eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977135"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a>Evitar el cierre de sesión o suspender durante una grabación

Si no se toman las precauciones adecuadas dentro de una aplicación, es posible que un usuario cierre la sesión durante una operación de grabación. Esto conduce a la interrupción del proceso de grabación, lo que puede provocar la pérdida de datos y, posiblemente, hacer que el disco sea inutilizable.

Para evitar este problema, la aplicación debe procesar el [**mensaje WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) que se entrega antes de cerrar la sesión. Si la aplicación recibe este mensaje mientras realiza una operación de grabación, devuelva **FALSE** para cancelar el procedimiento de cierre de sesión. Si la aplicación permite al usuario decidir si desea continuar con el registro, se debe proporcionar una advertencia que indique que el usuario perderá datos.

Las transiciones de energía durante el proceso de grabación también pueden crear posibles problemas en el éxito de una actividad de grabación. Evitar estas complicaciones durante el proceso de grabación requiere que una aplicación tenga en cuenta cuándo se van a realizar las transiciones de energía. Esto se logra habilitando la aplicación para procesar el [**mensaje \_ WM POWERBROADCAST.**](/windows/desktop/Power/wm-powerbroadcast) Las aplicaciones desarrolladas para Windows XP o Windows Server 2003 pueden devolver **BROADCAST \_ QUERY \_ DENY** en respuesta a [**\_ PBT APMQUERYSUSPEND,**](/windows/desktop/Power/pbt-apmquerysuspend)lo que impide suspender durante el proceso de grabación.

Debido a los cambios en el modelo de administración de energía para Windows Vista y Windows Server 2008, el evento [**\_ PBT APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) ya no se entrega a las aplicaciones. En su lugar, se entrega el evento [**\_ PBT APMSUSPEND,**](/windows/desktop/Power/pbt-apmsuspend) lo que proporciona dos segundos para que una aplicación se prepare para la transición.

Como resultado de estos cambios, se recomienda que las aplicaciones llamen a la función [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) para evitar un tiempo de espera de inactividad del sistema que normalmente da lugar a la transición a Suspender. Es importante recordar que llamar a esta función con las marcas adecuadas establecidas solo evitará la inactividad del sistema, no una suspensión en curso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de IMAPI](using-imapi.md)
</dt> <dt>

[**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 