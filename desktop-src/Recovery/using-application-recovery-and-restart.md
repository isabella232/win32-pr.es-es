---
title: Uso de la recuperación y reinicio de aplicaciones
description: Una aplicación puede usar la recuperación y el reinicio de la aplicación (ARR) para guardar los datos y la información de estado antes de que se cierre la aplicación debido a una excepción no controlada o cuando la aplicación deja de responder. También se reinicia la aplicación, si se solicita.
ms.assetid: 28cbb4c0-a287-4302-b3a9-daddc69adb40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5bf0b9bd0e0f6cc257ee785ab5df6febc8fef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904640"
---
# <a name="using-application-recovery-and-restart"></a>Uso de la recuperación y reinicio de aplicaciones

Una aplicación puede usar la recuperación y el reinicio de la aplicación (ARR) para guardar los datos y la información de estado antes de que se cierre la aplicación debido a una excepción no controlada o cuando la aplicación deja de responder. También se reinicia la aplicación, si se solicita.

Al registrarse para la recuperación o el reinicio, se agrega la información de registro al proceso. [Informe de errores de Windows (WER)](/windows/desktop/wer/windows-error-reporting) utiliza la información de registro para llamar a la devolución de llamada de recuperación y reiniciar la aplicación. Por ejemplo, si se registra para la recuperación y la aplicación encuentra una excepción no controlada, WER muestra un cuadro de diálogo al usuario que ofrece al usuario la opción de comprobar una solución en línea, cerrar el programa o depurar el programa. Si el usuario elige buscar una solución o cerrar el programa, WER llama a la devolución de llamada registrada y proporciona a la aplicación la oportunidad de guardar los datos y la información de estado. Una vez finalizada la recuperación, se finaliza la aplicación.

Si se registra para el reinicio y la aplicación encuentra una excepción no controlada, WER muestra el mismo cuadro de diálogo al usuario, pero ofrece la opción de reiniciar el programa en lugar de cerrar el programa. Si se registra para la recuperación y el reinicio, se produce primero la recuperación; a continuación, la aplicación se termina y se reinicia.

Una aplicación que no responde se administra de manera similar. Una aplicación se considera que no responde si no responde a los mensajes de Windows durante cinco segundos y el usuario intenta interactuar con la aplicación. el usuario verá (no responde) en la barra de título. WER se activa cuando el usuario hace clic en el botón Cerrar del sistema.

Debe registrarse para recuperar o reiniciar, o bien quitar el registro, antes de que la aplicación deje de responder o encuentre una excepción no controlada. Sin embargo, en la devolución de llamada de recuperación, puede cambiar la línea de comandos de reinicio.

Para obtener más información sobre el registro para la recuperación o el reinicio, vea los temas siguientes:

-   [Registro para la recuperación de la aplicación](registering-for-application-recovery.md)
-   [Registrando el reinicio de la aplicación](registering-for-application-restart.md)

Para obtener ejemplos que implementan las características de recuperación y reinicio, vea los ejemplos de AppRecovery y AppRestart en el Windows SDK ubicado en la \\ carpeta Winbase WindowsErrorReporting.

 

 