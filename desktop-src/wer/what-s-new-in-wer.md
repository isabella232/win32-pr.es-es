---
title: Novedades de WER
description: En esta página se resumen las nuevas características de Informe de errores de Windows (WER) de cada versión.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Informe de errores de Windows Informe de errores de Windows, novedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358811"
---
# <a name="whats-new-in-wer"></a>Novedades de WER

En esta página se resumen las nuevas características de Informe de errores de Windows (WER) de cada versión.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

En la lista siguiente se resumen las nuevas características de WER para Windows 7 y Windows Server 2008 R2.

-   Agrega la capacidad de producir una excepción que omite todos los controladores de excepciones y, por tanto, finaliza la aplicación inmediatamente e invoca Informe de errores de Windows. Para obtener más información, consulte la función [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) .
-   Agrega la capacidad de registrar un controlador de excepciones fuera de proceso al que WER llama cuando se produce un bloqueo para recopilar el nombre del evento, los parámetros de informes y las opciones de inicio de depuración. Para obtener más información, consulte la función [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) .

Funciones que se agregaron:

-   [**OutOfProcessExceptionEventCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [**OutOfProcessExceptionEventSignatureCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [**OutOfProcessExceptionEventDebuggerLaunchCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))
-   [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [**WerUnregisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

Estructuras agregadas:

-   [**\_información de \_ excepción en tiempo de ejecución de Wer \_**](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 y Windows Vista SP1

En la lista siguiente se resumen las nuevas características de WER para Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

-   WER puede configurarse para que los volcados de modo de usuario completos se recopilen y almacenen localmente después de que una aplicación de modo de usuario se bloquee (no se admiten las aplicaciones que realizan sus propios informes de bloqueo personalizados, incluidas las aplicaciones .NET). Para obtener más información, consulte [recopilación de volcados de User-Mode](collecting-user-mode-dumps.md).

## <a name="windows-vista"></a>Windows Vista

En la lista siguiente se resumen las nuevas características de Informe de errores de Windows (WER) para Windows Vista:

-   WER se ha extendido más allá de los bloqueos de supervisión y los procesos que no responden. WER incluye compatibilidad con muchos nuevos tipos de eventos no críticos, como problemas de rendimiento. Esto permite a los desarrolladores obtener más información sobre las experiencias que tienen sus clientes con las aplicaciones que han desarrollado.
-   Las nuevas funciones proporcionan a los desarrolladores la flexibilidad necesaria para crear, personalizar y enviar informes de problemas. Para obtener más información, vea [funciones wer](wer-functions.md).
-   Los [servicios en línea de calidad de Windows](https://www.microsoft.com/?ref=go) mejorados proporcionan a los desarrolladores acceso a la información de problemas que los clientes envían para sus aplicaciones y un mecanismo para ofrecer soluciones a estos clientes.
-   Las funciones introducidas por la [recuperación de aplicaciones y](/windows/desktop/Recovery/application-recovery-and-restart-portal) el [Administrador](/windows/desktop/RstMgr/restart-manager-portal) de reinicio y reinicio permiten a las aplicaciones recuperar información automáticamente y reiniciarse en caso de un error crítico. Los desarrolladores pueden usar estas características en sus aplicaciones para mejorar significativamente la experiencia del usuario.
-   **Informes de problemas y soluciones en Windows Vista o en el centro de actividades de Windows 7** es la ubicación central para que los usuarios interactúen con wer. Los usuarios pueden buscar nuevas soluciones, administrar su historial de informes, ver los detalles de un informe de problemas y administrar la configuración de informes, incluida la habilitación de WER para buscar soluciones automáticamente sin interrumpir al usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Informe de errores de Windows](windows-error-reporting.md)
</dt> </dl>

 

 