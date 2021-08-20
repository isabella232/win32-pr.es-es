---
description: En la tabla siguiente se resumen las diferencias entre el apagado en Windows Vista y Windows XP.
ms.assetid: da7985d2-85c8-47e1-a172-c9e92f450e24
title: Cambios de apagado para Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd510e800de23c2304dbc8c61b6547f9f3e846002b234401d0b8e3d0bbaa820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963562"
---
# <a name="shutdown-changes-for-windows-vista"></a>Cambios de apagado para Windows Vista

En la tabla siguiente se resumen las diferencias entre el apagado en Windows Vista y Windows XP.



| Característica                 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                | Windows Vista                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bloqueo del cierre       | Las aplicaciones pueden retrasar la respuesta [**a WM \_ QUERYENDSESSION**](wm-queryendsession.md) durante 5 segundos y, a continuación, el sistema permite al usuario finalizar la aplicación. Las aplicaciones que **devuelven TRUE** en respuesta a **WM \_ QUERYENDSESSION** pueden retrasar la respuesta a [**WM \_ ENDSESSION**](wm-endsession.md) durante 5 segundos y, a continuación, el sistema permite al usuario finalizar la aplicación. | Las aplicaciones pueden retrasar la respuesta [**a WM \_ QUERYENDSESSION**](wm-queryendsession.md) durante 5 segundos y, a continuación, el sistema permite al usuario continuar o cancelar el apagado. Las aplicaciones que **devuelven TRUE** en respuesta a **WM \_ QUERYENDSESSION** pueden retrasar la respuesta a [**WM \_ ENDSESSION**](wm-endsession.md) durante 5 segundos y, a continuación, el sistema permite al usuario continuar o cancelar el apagado.                                                                                                      |
| Cancelación del apagado      | Si una aplicación devuelve **FALSE en** respuesta a [**WM \_ QUERYENDSESSION,**](wm-queryendsession.md)el cierre se cancela en la mayoría de los casos. Sin embargo, no se muestra ninguna interfaz de usuario, por lo que es posible que el usuario no tenga en cuenta que se ha cancelado el apagado.                                                                                                                                                      | Si una aplicación devuelve **FALSE en respuesta** a WM [**\_ QUERYENDSESSION,**](wm-queryendsession.md)todavía aparece en la interfaz de usuario de apagado. Tenga en cuenta que el sistema no permite que las aplicaciones de consola o las aplicaciones sin una ventana visible cancelen el apagado. Estas aplicaciones se finalizan automáticamente si no responden a **WM \_ QUERYENDSESSION** o [**WM \_ ENDSESSION**](wm-endsession.md) en un plazo de 5 segundos o si **devuelven FALSE** en respuesta a WM **\_ QUERYENDSESSION**. |
| Apagar la interfaz de usuario | El sistema muestra un cuadro de diálogo para cada aplicación que bloquea el cierre. Si el usuario hace clic en **el botón End Now (Finalizar** ahora), la aplicación finaliza. Si el usuario hace clic en el **botón Cancelar,** se cancela el apagado y la aplicación continúa en ejecución.                                                                                                                                    | El sistema muestra una interfaz de usuario de pantalla completa que identifica todas las aplicaciones que bloquean el cierre y sus motivos para hacerlo (si han registrado un motivo mediante [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)).                                                                                                                                                                                                                                                                    |



 

## <a name="best-practices"></a>Prácticas recomendadas

-   Las aplicaciones no deben bloquear el apagado. Responda a [**WM \_ QUERYENDSESSION lo**](wm-queryendsession.md) antes posible y posponga las actividades de limpieza hasta que procese el mensaje DE WM [**\_ ENDSESSION.**](wm-endsession.md)
-   Las aplicaciones que deben bloquear el apagado deben usar la nueva [**función ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) para registrar una cadena que explique el motivo para el usuario. El usuario puede decidir si desea continuar o cancelar el apagado.
-   Las aplicaciones no pueden confiar en poder bloquear el apagado.

 

 



