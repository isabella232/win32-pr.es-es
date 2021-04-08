---
description: El servicio Programador de clases multimedia (MMCSS) permite a las aplicaciones multimedia asegurarse de que su procesamiento dependiente del tiempo recibe un acceso prioritario a los recursos de la CPU.
ms.assetid: a7169938-1c72-4c4c-881a-cb08ad6182c7
title: Servicio del programador de clases multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80656276af30495c084d0964534a04e11896bcd2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003348"
---
# <a name="multimedia-class-scheduler-service"></a>Servicio del programador de clases multimedia

El servicio Programador de clases multimedia (MMCSS) permite a las aplicaciones multimedia asegurarse de que su procesamiento dependiente del tiempo recibe un acceso prioritario a los recursos de la CPU. Este servicio permite a las aplicaciones multimedia emplear la mayor parte de la CPU posible sin denegar recursos de CPU a aplicaciones de menor prioridad.

MMCSS usa la información almacenada en el registro para identificar las tareas admitidas y determinar la prioridad relativa de los subprocesos que realizan estas tareas. Cada subproceso que está realizando trabajo relacionado con una tarea determinada llama a la función [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) o [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa) para informar a MMCSS de que está trabajando en esa tarea.

Para ver un ejemplo de un programa que usa MMCSS, consulte [flujos de modo exclusivo](/previous-versions//bb614507(v=vs.85)).

**Windows Server 2003 y Windows XP:** MMCSS no está disponible.

## <a name="registry-settings"></a>Configuración del Registro

La configuración de MMCSS se almacena en la siguiente clave del registro:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ multimedia \\ SystemProfile**

Esta clave contiene un valor de **reg \_ DWORD** denominado **SystemResponsiveness** que determina el porcentaje de recursos de CPU que se deben garantizar en tareas de prioridad baja. Por ejemplo, si este valor es 20, el 20% de los recursos de CPU se reservan para las tareas de prioridad baja. Tenga en cuenta que los valores que no se pueden dividir uniformemente por 10 se redondean al múltiplo más próximo de 10. Un valor de 0 también se trata como 10.

La clave también contiene una subclave denominada **Tasks** que contiene la lista de tareas. De forma predeterminada, Windows admite las siguientes tareas:

-   **Audio**
-   **Capture**
-   **Distribución**
-   **Juegos**
-   **Reproducción**
-   **Audio de Pro**
-   **Administrador de ventanas**

Los OEM pueden agregar tareas adicionales según sea necesario.

Cada clave de tarea contiene el siguiente conjunto de valores que representan las características que se van a aplicar a los subprocesos que están asociados a la tarea.

| Value                   | Formato         | Valores posibles                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Afinidad**            | **\_valor DWORD reg** | Máscara de máscara que indica la afinidad del procesador. Tanto 0x00 como 0xFFFFFFFF indican que no se utiliza la afinidad del procesador.                                                                                                                                                                                                                                                 |
| **Solo en segundo plano**     | **Registro \_ SZ**    | Indica si se trata de una tarea en segundo plano (sin interfaz de usuario). Los subprocesos de una tarea en segundo plano no cambian debido a un cambio en el foco de la ventana. Este valor se puede establecer en true o false.                                                                                                                                                                            |
| **BackgroundPriority**  | **\_valor DWORD reg** | Prioridad de fondo. El intervalo de valores es 1-8.                                                                                                                                                                                                                                                                                                                    |
| **Frecuencia del reloj**          | **\_valor DWORD reg** | Sugerencia usada por MMCSS para determinar la granularidad de la programación de recursos del procesador. **Windows Server 2008 y Windows Vista:** La tasa de reloj máxima garantizada que el sistema utiliza si un subproceso se une a esta tarea en intervalos de 100 segundos. A partir de Windows 7 y Windows Server 2008 R2, esta garantía se ha quitado para reducir el consumo de energía del sistema.<br/> |
| **Prioridad de GPU**        | **\_valor DWORD reg** | Prioridad de la GPU. El intervalo de valores es 0-31. Esta prioridad no se ha utilizado todavía.                                                                                                                                                                                                                                                                                           |
| **Prioridad**            | **\_valor DWORD reg** | Prioridad de la tarea. El intervalo de valores es de 1 (baja) a 8 (alto). En el caso de las tareas con una **categoría de programación** de alto, este valor siempre se trata como 2.<br/>                                                                                                                                                                                                           |
| **Categoría de programación** | **Registro \_ SZ**    | Categoría de programación. Este valor se puede establecer en alto, medio o bajo.                                                                                                                                                                                                                                                                                                 |
| **Prioridad de SFIO**       | **Registro \_ SZ**    | Prioridad de e/s programada. Este valor se puede establecer en Idle, Low, normal o High. Este valor no se utiliza.                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Para ahorrar energía, las aplicaciones no deben establecer la resolución del temporizador en todo el sistema en un valor pequeño a menos que sea absolutamente necesario. Para obtener más información, vea [rendimiento](../win7devguide/performance.md) en la [Guía para desarrolladores de Windows 7](../win7devguide/windows-7-developer-guide.md).

 

## <a name="thread-priorities"></a>Prioridades de subprocesos

MMCSS aumenta la prioridad de los subprocesos que trabajan en tareas multimedia de alta prioridad.

MMCSS determina la prioridad de un subproceso mediante los siguientes factores:

-   La prioridad base de la tarea.
-   Parámetro *Priority* de la función [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority) .
-   Indica si la aplicación está en primer plano.
-   Cantidad de tiempo de CPU consumida por los subprocesos de cada categoría.

MMCSS establece la prioridad de los subprocesos de cliente en función de su categoría de programación.

| Category | Prioridad | Descripción                                                                                                                               |
|----------|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Alto     | 23-26    | Estos subprocesos se ejecutan con una prioridad de subproceso que es menor que solo ciertas tareas de nivel de sistema. Esta categoría está diseñada para las tareas de audio Pro. |
| Media   | 16-22    | Estos subprocesos forman parte de la aplicación que está en primer plano.                                                                      |
| Bajo      | 8-15     | Esta categoría contiene el resto de los subprocesos. Se garantiza un porcentaje mínimo de los recursos de la CPU si es necesario.           |
|          | 1-7      | Estos subprocesos han usado su cuota de recursos de CPU. Pueden continuar ejecutándose si no hay subprocesos de prioridad baja listos para ejecutarse.                |



 

 

 
