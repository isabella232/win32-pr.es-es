---
title: Uso de WER
description: A partir de Windows Vista, Windows proporciona informes de errores de bloqueo, no respuesta y error del kernel de forma predeterminada sin necesidad de realizar cambios en la aplicación.
ms.assetid: c096cd89-e3a7-4959-a35f-40e6168f277e
keywords:
- Windows informes de errores Informe de errores de Windows , mediante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17dfa8bc2235f43770cd177ad3e5d9a7d1aacde36034152b88cb06af3879e8c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442259"
---
# <a name="using-wer"></a>Uso de WER

A partir de Windows Vista, Windows proporciona informes de errores de bloqueo, no respuesta y error del kernel de forma predeterminada sin necesidad de realizar cambios en la aplicación. El informe incluirá información de minivolcación y volcado de montón si es necesario. En su lugar, las aplicaciones usan la API de WER para enviar informes de problemas específicos de la aplicación a Microsoft.

Dado Windows notifica automáticamente excepciones no controladas, la aplicación no debe controlar las excepciones irreales. Si el proceso de error o no responde es interactivo, WER muestra una interfaz de usuario que informa al usuario del problema. Una aplicación se considera que no responde si no responde Windows mensajes durante cinco segundos mientras el usuario intenta interactuar con la aplicación.

## <a name="windows-error-reporting-flow-for-crashes-non-response-and-kernel-faults"></a>Informe de errores de Windows en caso de bloqueos, falta de respuesta y errores de kernel

A continuación se muestran los pasos que se producen para un bloqueo de la aplicación, una falta de respuesta o un error de kernel.

1.  Se produce el evento de problema.
2.  El sistema operativo invoca WER.
3.  WER recopila los datos, compila un informe y solicita al usuario su consentimiento (si es necesario).
4.  WER envía el informe a Microsoft (Watson Server) si el usuario ha dado su consentimiento.
5.  Si el servidor Watson solicita datos adicionales, WER recopila los datos y solicita al usuario su consentimiento (si es necesario).
6.  Si la aplicación se ha registrado para la recuperación y el reinicio, WER ejecuta las funciones de devolución de llamada registradas mientras los datos se comprimen y se envían a Microsoft (si el usuario ha dado su consentimiento).
7.  Si hay una respuesta al problema disponible en Microsoft, se notifica al usuario.

Las aplicaciones pueden usar las siguientes funciones para personalizar el contenido del informe que se envía a Microsoft. Las funciones de registro le informan a WER de que incluya los archivos y bloques de memoria específicos en el informe de errores que crea.

-   [**WerRegisterFile**](/windows/desktop/api/Werapi/nf-werapi-werregisterfile)
-   [**WerRegisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werregistermemoryblock)
-   [**WerSetFlags**](/windows/desktop/api/Werapi/nf-werapi-wersetflags)
-   [**WerUnregisterFile**](/windows/desktop/api/Werapi/nf-werapi-werunregisterfile)
-   [**WerUnregisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werunregistermemoryblock)
-   [**WerGetFlags**](/windows/desktop/api/Werapi/nf-werapi-wergetflags)

## <a name="windows-error-reporting-flow-for-generic-event-reporting"></a>Informe de errores de Windows para informes de eventos genéricos

En los pasos siguientes se muestra cómo las aplicaciones pueden obtener un informe de errores para una condición de error no grave.

1.  Se produce el evento de problema no grave.
2.  La aplicación reconoce el evento y usa la siguiente secuencia de llamadas de función para generar el informe.
    1.  Llame a [**la función WerReportCreate**](/windows/desktop/api/Werapi/nf-werapi-werreportcreate) para crear el informe.
    2.  Llame a [**la función WerReportSetParameter**](/windows/desktop/api/Werapi/nf-werapi-werreportsetparameter) para establecer los parámetros del informe.
    3.  Llame a [**la función WerReportAddFile**](/windows/desktop/api/Werapi/nf-werapi-werreportaddfile) para agregar archivos al informe.
    4.  Llame a [**la función WerReportAddDump**](/windows/desktop/api/Werapi/nf-werapi-werreportadddump) para agregar un minivolfón al informe (si es necesario).
    5.  Llame a [**la función WerReportSubmit**](/windows/desktop/api/Werapi/nf-werapi-werreportsubmit) para enviar el informe.
    6.  Llame a [**WerReportCloseHandle para**](/windows/desktop/api/Werapi/nf-werapi-werreportclosehandle) liberar recursos.
3.  En función de las opciones específicas usadas al llamar a las funciones del paso 2, WER finalizará los informes de errores. WER garantizará que los informes se realizan de acuerdo con las directivas establecidas por el usuario. Por ejemplo, WER enviará el informe a Microsoft, pondrá en cola el informe y mostrará las interfaces de usuario adecuadas al usuario.

## <a name="excluding-an-application-from-windows-error-reporting"></a>Excluir una aplicación de Informe de errores de Windows

Para excluir la aplicación de Windows informes de errores, use la [**función WerAddExcludedApplication.**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication) Para restaurar los informes de errores de la aplicación, use la [**función WerRemoveExcludedApplication.**](/windows/desktop/api/Werapi/nf-werapi-werremoveexcludedapplication)

## <a name="automatically-recovering-data-and-restarting-a-faulted-application"></a>Recuperación automática de datos y reinicio de una aplicación con errores

Una aplicación puede usar Application Recovery y Restart para guardar datos y la información de estado antes de que la aplicación se cierre debido a una excepción no controlada o cuando la aplicación deje de responder. La aplicación también se reinicia, si se solicita. Para más información, consulte [Recuperación y reinicio de aplicaciones.](/windows/desktop/Recovery/application-recovery-and-restart-portal)

## <a name="legacy-api"></a>API heredada

Una aplicación puede notificar un error llamando a la [**función ReportFault.**](/windows/desktop/api/ErrorRep/nf-errorrep-reportfault) Sin embargo, no debe usar la función **ReportFault** a menos que tenga un requisito muy específico que no pueda cumplir el comportamiento predeterminado de informes de errores del sistema operativo.

Si está habilitado el informe de errores, el sistema muestra un cuadro de diálogo al usuario que indica que la aplicación ha detectado un problema y se cerrará. Si hay un depurador configurado en la clave **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ AeDebug,** el usuario tiene la opción de iniciar el depurador. El usuario también tiene la opción de enviar un informe a Microsoft. Si el usuario envía el informe, el sistema muestra otro cuadro de diálogo que da las gracias al usuario por el informe y proporciona un vínculo a más información.

El sistema de informes de errores admite los siguientes modos de operación.



| Modo de operación          | Descripción                                                                                                                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Informes de memoria compartida | Si el contexto de seguridad de la aplicación es el mismo que el contexto de seguridad del usuario que ha iniciado sesión, el sistema de informes de errores usa un bloque de memoria compartida para la comunicación. Este modo no se puede usar con el modo de informes de manifiesto.<br/>                                                                                               |
| Informes de manifiestos      | Si el contexto de seguridad de la aplicación no es el mismo que el contexto de seguridad del usuario que ha iniciado sesión, el sistema de informes de errores usa un archivo para la comunicación. Este modo también se usa para notificar aplicaciones que no responden y errores de kernel. Este modo no se puede usar con el modo de informes de memoria compartida.<br/>                      |
| Informes de Internet      | El sistema de informes de errores envía todos los datos a Microsoft a través de Internet. Este es el modo de funcionamiento predeterminado. No se puede usar con el modo de informes corporativos. Este modo se usa cuando el administrador no especifica ninguna ruta de acceso de carga corporativa.<br/>                                                                     |
| Informes corporativos     | El sistema de informes de errores envía todos los datos a un recurso compartido de archivos en lugar de cargarlos directamente en Microsoft. Esto permite a los administradores de TI corporativos revisar los datos antes de enviarse a Microsoft. Este modo se usa cuando hay una ruta de acceso de carga corporativa especificada por el administrador. No se puede usar con el modo de informes de Internet.<br/> |
| Informes sin sentido      | El sistema de informes de errores no mostrará ningún cuadro de diálogo al usuario. Esto permite a los administradores de TI corporativos recopilar informes de errores de sus empleados en todo momento. Este modo se usa cuando el administrador habilita los informes, pero la notificación está deshabilitada. Solo se puede usar con el modo de informes corporativos.<br/>        |



 

Para excluir la aplicación de los informes de errores, use [**la función AddERExcludedApplication.**](/windows/desktop/api/ErrorRep/nf-errorrep-adderexcludedapplicationa)

 

