---
description: Calidad de servicio indica el rendimiento y la eficacia de energía de un subproceso, lo que puede influir en la programación de subprocesos y en la administración de energía del procesador.
title: Calidad de servicio
ms.topic: article
ms.date: 07/09/2021
ms.openlocfilehash: ec4e92360d23a427d526a36a81bfdb0667c1cb6fb5f60ddcefd578c4918ba5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793469"
---
# <a name="quality-of-service"></a>Calidad de servicio

La calidad de servicio (QoS) asociada a un subproceso se usa para indicar el rendimiento y la eficacia de energía deseados. Cada subproceso se asigna a un nivel de QoS. Aunque la prioridad de programación sigue siendo la métrica principal por la que el sistema determina qué subproceso programar a continuación, QoS puede influir en la selección de núcleos y la administración de energía del procesador. En las plataformas con procesadores heterogéneos, la QoS de un subproceso puede restringir la programación a un subconjunto de procesadores o indicar una preferencia para una clase determinada de procesador.

Es posible que los desarrolladores ya empleen otras instalaciones para controlar cuándo se debe ejecutar, por ejemplo, cuando el usuario no está presente, solo en ac/carga, o en función del nivel de batería. QoS proporciona una instalación para influir en cómo ejecutar. Esta instalación puede ayudar a mejorar la eficacia de la CPU y, por tanto, a ampliar la duración de la batería. Además, este proceso puede ayudar a reducir el consumo de energía de CPU mientras se utiliza la alimentación de CA para reducir la salida térmico, lo que puede provocar un alto ruido del ventilador o incluso una limitación térmico.

## <a name="quality-of-service-levels"></a>Niveles de calidad de servicio

El sistema mantiene varios niveles de QoS, cada uno con rendimiento diferenciado y eficiencia energética. Windows proporciona la configuración predeterminada estándar para la programación y la administración de energía del procesador para cada nivel de QoS. El ajuste preciso de cada nivel de QoS para la administración de energía del procesador y la programación heterogéneo se puede modificar mediante Windows Provisioning. Para más información sobre la optimización y el aprovisionamiento del rendimiento, consulte [Opciones de administración de energía del procesador.](/windows-hardware/customize/power-settings/configure-processor-power-management-options)

| Nivel de QoS | Descripción|Rendimiento y potencia | Release |
| --- | --- | --- | --- |
| Alto | Aplicaciones en ventanas que se encuentran en primer plano y en el foco, o son sonables, y etiquetan explícitamente procesos con [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) o subprocesos [con SetThreadInformation](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation) | Alto rendimiento estándar. |1709 |
| Media | Aplicaciones en ventanas que pueden ser visibles para el usuario final, pero que no están en el foco. | Varía según la plataforma, entre Alta y Baja. | 1709 |
| Bajo | Aplicaciones en ventanas que no son visibles ni son visibles para el usuario final. | En batería, selecciona la frecuencia de CPU más eficaz y programa el núcleo eficiente. | 1709 |
| Eco | Aplicaciones que etiquetan explícitamente procesos [con SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) o subprocesos [con SetThreadInformation.](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation) | Siempre selecciona la frecuencia de CPU y programaciones más eficaces para núcleos eficientes. | Windows 11 |
| Medios | Subprocesos etiquetados explícitamente por el servicio Programador de [clases multimedia](/windows/desktop/procthread/multimedia-class-scheduler-service) para indicar el almacenamiento en búfer por lotes multimedia. | Frecuencia de CPU reducida para un procesamiento por lotes eficaz. | 2004 |
| Fecha límite | Subprocesos etiquetados explícitamente por el servicio Programador de [clases multimedia](/windows/desktop/procthread/multimedia-class-scheduler-service) para indicar que los subprocesos de audio requieren rendimiento para cumplir las fechas límite. | Alto rendimiento para cumplir las fechas límite de los medios. | 2004 |

## <a name="quality-of-service-classification"></a>Clasificación de calidad de servicio

En la tabla siguiente se muestran las clasificaciones de QoS admitidas.

| Origen | Descripción |
| --- | --- |
| Multimedia Foundation | El [servicio Programador de clases multimedia da](/windows/desktop/procthread/multimedia-class-scheduler-service) prioridad a los recursos de CPU para escenarios multimedia. El servicio etiqueta subprocesos específicos responsables del procesamiento multimedia mediante los niveles Media y Deadline QoS para proporcionar eficiencia energética al tiempo que se cumplen las fechas límite de rendimiento.  |
| API | [SetProcessInformation permite](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) a los desarrolladores etiquetar explícitamente un proceso como HighQoS o EcoQoS al alternar la característica `PROCESS_POWER_THROTTLING_EXECUTION_SPEED` en **ProcessPowerThrottling**.</br>[SetThreadInformation permite](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) a los desarrolladores etiquetar explícitamente un subproceso como HighQoS o EcoQoS al alternar la característica en `THREAD_POWER_THROTTLING_EXECUTION_SPEED` **ThreadPowerThrottling** .  |
| Audible | Los procesos que se determinan para reproducir audio son HighQoS. |
| Visible | A los procesos que poseen directamente una ventana (o son descendientes de procesos propietarios de ventanas) se les asigna un nivel de QoS según su visibilidad y estado de foco:</br></br><table><tr><th>Estado de la ventana</th><th>Calidad de servicio</th></tr><tr><td>En foco</td><td>Alto</td></tr><tr><td>Visible</td><td>Media</td></tr><tr><td>Minimizado o totalmente ocluido</td><td>Bajo</td></tr></table> |
| Método heurístico | El sistema asigna automáticamente un nivel de QoS a los subprocesos que no están clasificados por los orígenes anteriores. Estas heurísticas incluyen (pero no se limitan a) la prioridad de subproceso, donde los subprocesos que se ejecutan con prioridad de subproceso reducida pueden implicar un nivel de QoS inferior. |
