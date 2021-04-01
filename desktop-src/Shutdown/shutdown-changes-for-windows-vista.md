---
description: En la tabla siguiente se resumen las diferencias entre el apagado de Windows Vista y Windows XP.
ms.assetid: da7985d2-85c8-47e1-a172-c9e92f450e24
title: Cambios de apagado de Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e04bb20099349ce378384cf01c39e53ca03a896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082703"
---
# <a name="shutdown-changes-for-windows-vista"></a>Cambios de apagado de Windows Vista

En la tabla siguiente se resumen las diferencias entre el apagado de Windows Vista y Windows XP.



| Característica                 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                | Windows Vista                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bloqueo de cierre       | Las aplicaciones pueden retrasar la respuesta a [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) durante 5 segundos y, a continuación, el sistema permite al usuario finalizar la aplicación. Las aplicaciones que devuelven **true** en respuesta a **WM \_ QUERYENDSESSION** pueden retrasar la respuesta a [**WM \_ ENDSESSION**](wm-endsession.md) durante 5 segundos, de modo que el sistema permite al usuario finalizar la aplicación. | Las aplicaciones pueden retrasar la respuesta a [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) durante 5 segundos y, a continuación, el sistema permite al usuario continuar o cancelar el cierre. Las aplicaciones que devuelven **true** en respuesta a **WM \_ QUERYENDSESSION** pueden retrasar la respuesta a [**WM \_ ENDSESSION**](wm-endsession.md) durante 5 segundos, por lo que el sistema permite al usuario continuar o cancelar el cierre.                                                                                                      |
| Cancelando apagado      | Si una aplicación devuelve **false** en respuesta a [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), el cierre se cancela en la mayoría de los casos. Sin embargo, no se muestra ninguna interfaz de usuario, por lo que es posible que el usuario no tenga en cuenta que se ha cancelado el cierre.                                                                                                                                                      | Si una aplicación devuelve **false** en respuesta a [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), sigue apareciendo en la interfaz de usuario de apagado. Tenga en cuenta que el sistema no permite que las aplicaciones de consola o las aplicaciones sin una ventana visible cancele el cierre. Estas aplicaciones se terminan automáticamente si no responden a **WM \_ QUERYENDSESSION** o a [**WM \_ ENDSESSION**](wm-endsession.md) en 5 segundos o si devuelven **false** en respuesta a **WM \_ QUERYENDSESSION**. |
| Apagar la interfaz de usuario | El sistema muestra un cuadro de diálogo para cada aplicación que bloquea el cierre. Si el usuario hace clic en el botón **finalizar ahora** , la aplicación se termina. Si el usuario hace clic en el botón **Cancelar** , se cancela el cierre y la aplicación continúa ejecutándose.                                                                                                                                    | El sistema muestra una interfaz de usuario de pantalla completa que identifica todas las aplicaciones que bloquean el cierre y sus motivos para hacerlo (si han registrado un motivo mediante [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)).                                                                                                                                                                                                                                                                    |



 

## <a name="best-practices"></a>Prácticas recomendadas

-   Las aplicaciones no deben bloquear el cierre. Responder a [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) lo más rápido posible y posponer las actividades de limpieza hasta que se procese el mensaje de la [**\_ ENDSESSION de WM**](wm-endsession.md) .
-   Las aplicaciones que deben bloquear el cierre deben usar la nueva función [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) para registrar una cadena que explique el motivo para el usuario. El usuario puede decidir si desea continuar o cancelar el apagado.
-   Las aplicaciones no pueden basarse en la posibilidad de bloquear el cierre.

 

 



