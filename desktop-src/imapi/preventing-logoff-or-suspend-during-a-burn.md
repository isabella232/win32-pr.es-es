---
title: Evitar el cierre de sesión o la suspensión durante una grabación
description: Si las precauciones adecuadas no se realizan dentro de una aplicación, es posible que un usuario cierre la sesión durante una operación de grabación. Esto conduce a la interrupción del proceso de grabación, lo que puede provocar la pérdida de datos y posiblemente que el disco no se pueda usar.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5922fbe6dbc27303cee82e7ed745cbaaf2744781
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487599"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a>Evitar el cierre de sesión o la suspensión durante una grabación

Si las precauciones adecuadas no se realizan dentro de una aplicación, es posible que un usuario cierre la sesión durante una operación de grabación. Esto conduce a la interrupción del proceso de grabación, lo que puede provocar la pérdida de datos y posiblemente que el disco no se pueda usar.

Para evitar este problema, la aplicación debe procesar el mensaje de [**\_ QUERYENDSESSION de WM**](/windows/desktop/Shutdown/wm-queryendsession) que se entrega antes de cerrar la sesión. Si la aplicación recibe este mensaje mientras realiza una operación de grabación, devuelva **false** para cancelar el procedimiento de cierre de sesión. Si la aplicación permite al usuario decidir si desea continuar con el cierre de sesión, se debe proporcionar una advertencia que indica que el usuario perderá los datos.

Las transiciones de energía durante el proceso de grabación también pueden crear posibles problemas en el éxito de una actividad de grabación. Para evitar estas complicaciones durante el proceso de grabación, es necesario que una aplicación tenga en cuenta Cuándo están a punto de realizarse las transiciones de energía. Esto se logra mediante la habilitación de la aplicación para procesar el mensaje de [**\_ POWERBROADCAST de WM**](/windows/desktop/Power/wm-powerbroadcast) . Las aplicaciones desarrolladas para Windows XP o Windows Server 2003 pueden devolver la **consulta de difusión \_ \_ Deny** en respuesta a [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend), lo que impide la suspensión durante el proceso de grabación.

Debido a los cambios en el modelo de administración de energía de Windows Vista y Windows Server 2008, el evento [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) ya no se entrega a las aplicaciones. En su lugar, se entrega el evento [**PBT \_ APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) , que proporciona dos segundos para que una aplicación se prepare para la transición.

Como resultado de estos cambios, se recomienda que las aplicaciones llamen a la función [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) para evitar un tiempo de espera de inactividad del sistema que, normalmente, hace que la transición se suspenda. Es importante recordar que llamar a esta función con el conjunto de marcadores adecuado solo impedirá que el sistema esté inactivo, no una suspensión en curso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar IMAPi](using-imapi.md)
</dt> <dt>

[**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 