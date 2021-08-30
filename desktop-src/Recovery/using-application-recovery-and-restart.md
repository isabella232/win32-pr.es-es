---
title: Uso de la recuperación y el reinicio de aplicaciones
description: Una aplicación puede usar Recuperación y reinicio de aplicaciones (ARR) para guardar datos y información de estado antes de que la aplicación se cierre debido a una excepción no controlada o cuando la aplicación deje de responder. La aplicación también se reinicia, si se solicita.
ms.assetid: 28cbb4c0-a287-4302-b3a9-daddc69adb40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a844e7bb8795dae26fa2900b539651cdab3f07877dce83403bd37126dac197
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073655"
---
# <a name="using-application-recovery-and-restart"></a>Uso de la recuperación y el reinicio de aplicaciones

Una aplicación puede usar Recuperación y reinicio de aplicaciones (ARR) para guardar datos y información de estado antes de que la aplicación se cierre debido a una excepción no controlada o cuando la aplicación deje de responder. La aplicación también se reinicia, si se solicita.

Al registrarse para la recuperación o el reinicio, la información de registro se agrega al proceso. [Informe de errores de Windows (WER)](/windows/desktop/wer/windows-error-reporting) usa la información de registro para llamar a la devolución de llamada de recuperación y reiniciar la aplicación. Por ejemplo, si se registra para la recuperación y la aplicación encuentra una excepción no controlada, WER muestra un cuadro de diálogo al usuario que ofrece al usuario la opción de comprobar una solución en línea, cerrar el programa o depurar el programa. Si el usuario decide buscar una solución o cerrar el programa, WER llama a la devolución de llamada registrada y ofrece a la aplicación la oportunidad de guardar datos e información de estado. Una vez completada la recuperación, la aplicación finaliza.

Si se registra para reiniciar y la aplicación encuentra una excepción no controlada, WER muestra el mismo cuadro de diálogo al usuario, pero ofrece la opción de reiniciar el programa en lugar de cerrar el programa. Si se registra tanto para la recuperación como para el reinicio, la recuperación se produce primero. A continuación, la aplicación finaliza y se reinicia.

Una aplicación que no responde se controla de forma similar. Una aplicación se considera que no responde si no responde Windows mensajes durante cinco segundos y, a continuación, el usuario intenta interactuar con la aplicación. El usuario verá (No responder) en la barra de título. WER se activa cuando el usuario hace clic en el botón cerrar del sistema.

Debe registrarse para la recuperación o el reinicio, o quitar el registro, antes de que la aplicación deje de responder o encuentre una excepción no controlada. Sin embargo, en la devolución de llamada de recuperación, puede cambiar la línea de comandos de reinicio.

Para más información sobre cómo registrarse para la recuperación o el reinicio, consulte los temas siguientes:

-   [Registro para Application Recovery](registering-for-application-recovery.md)
-   [Registro para el reinicio de la aplicación](registering-for-application-restart.md)

Para obtener ejemplos que implementan las características de recuperación y reinicio, consulte los ejemplos AppRecovery y AppRestart en el SDK de Windows ubicado en la carpeta \\ WindowsErrorReporting de WinBase.

 

 