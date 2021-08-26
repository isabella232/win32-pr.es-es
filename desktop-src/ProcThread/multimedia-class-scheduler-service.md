---
description: El servicio Programador de clases multimedia (MMCSS) permite a las aplicaciones multimedia asegurarse de que su procesamiento con un tiempo limitado recibe acceso prioritario a los recursos de CPU.
ms.assetid: a7169938-1c72-4c4c-881a-cb08ad6182c7
title: Servicio Programador de clases multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0744883180c361d5656cf7c182f538d93617be7f6bbdc6a05ff93efa732b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032445"
---
# <a name="multimedia-class-scheduler-service"></a>Servicio Programador de clases multimedia

El servicio Programador de clases multimedia (MMCSS) permite a las aplicaciones multimedia asegurarse de que su procesamiento con un tiempo limitado recibe acceso prioritario a los recursos de CPU. Este servicio permite que las aplicaciones multimedia utilicen la mayor parte de la CPU posible sin denegar los recursos de CPU a las aplicaciones de prioridad inferior.

MMCSS usa la información almacenada en el Registro para identificar las tareas admitidas y determinar la prioridad relativa de los subprocesos que realizan estas tareas. Cada subproceso que realiza el trabajo relacionado con una tarea determinada llama a la función [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) o [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa) para informar a MMCSS de que está trabajando en esa tarea.

Para obtener un ejemplo de un programa que usa MMCSS, vea [Exclusive-Mode Secuencias](/previous-versions//bb614507(v=vs.85)).

**Windows Server 2003 y Windows XP:** MMCSS no está disponible.

## <a name="registry-settings"></a>Configuración del Registro

La configuración de MMCSS se almacena en la siguiente clave del Registro:

**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion Multimedia \\ \\ SystemProfile**

Esta clave contiene un **valor \_ REG DWORD** denominado **SystemResponsiveness** que determina el porcentaje de recursos de CPU que se deben garantizar para las tareas de prioridad baja. Por ejemplo, si este valor es 20, el 20 % de los recursos de CPU se reservan para tareas de prioridad baja. Tenga en cuenta que los valores que no se pueden dividir uniformemente entre 10 se redondea al múltiplo más cercano de 10. Un valor de 0 también se trata como 10.

La clave también contiene una subclave denominada **Tasks** que contiene la lista de tareas. De forma predeterminada, Windows admite las siguientes tareas:

-   **Audio**
-   **Capture**
-   **Distribución**
-   **Juegos**
-   **Reproducción**
-   **Pro Audio**
-   **Administrador de ventanas**

Los OEM pueden agregar tareas adicionales según sea necesario.

Cada clave de tarea contiene el siguiente conjunto de valores que representan las características que se van a aplicar a los subprocesos asociados a la tarea.

| Value                   | Formato         | Valores posibles                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Afinidad**            | **REG \_ DWORD** | Máscara de bits que indica la afinidad del procesador. Tanto 0x00 como 0xFFFFFFFF indican que no se usa la afinidad de procesador.                                                                                                                                                                                                                                                 |
| **Solo fondo**     | **REG \_ SZ**    | Indica si se trata de una tarea en segundo plano (sin interfaz de usuario). Los subprocesos de una tarea en segundo plano no cambian debido a un cambio en el foco de la ventana. Este valor se puede establecer en True o False.                                                                                                                                                                            |
| **BackgroundPriority**  | **REG \_ DWORD** | Prioridad en segundo plano. El intervalo de valores es 1-8.                                                                                                                                                                                                                                                                                                                    |
| **Frecuencia del reloj**          | **REG \_ DWORD** | Sugerencia usada por MMCSS para determinar la granularidad de la programación de recursos de procesador. **Windows Server 2008 y Windows Vista:** Velocidad de reloj máxima garantizada que usa el sistema si un subproceso se une a esta tarea, en intervalos de 100 nanosegundos. A partir Windows 7 y Windows Server 2008 R2, esta garantía se quitó para reducir el consumo de energía del sistema.<br/> |
| **Prioridad de GPU**        | **REG \_ DWORD** | Prioridad de GPU. El intervalo de valores es 0-31. Esta prioridad aún no se usa.                                                                                                                                                                                                                                                                                           |
| **Prioridad**            | **REG \_ DWORD** | Prioridad de la tarea. El intervalo de valores es de 1 (bajo) a 8 (alto). Para las tareas con **una categoría de programación** alta, este valor siempre se trata como 2.<br/>                                                                                                                                                                                                           |
| **Categoría de programación** | **REG \_ SZ**    | Categoría de programación. Este valor se puede establecer en Alto, Medio o Bajo.                                                                                                                                                                                                                                                                                                 |
| **Prioridad de SFIO**       | **REG \_ SZ**    | Prioridad de E/S programada. Este valor se puede establecer en Inactivo, Bajo, Normal o Alto. Este valor no se utiliza.                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Para ahorrar energía, las aplicaciones no deben establecer la resolución del temporizador de todo el sistema en un valor pequeño a menos que sea absolutamente necesario. Para obtener más información, vea [Rendimiento en](../win7devguide/performance.md) la guía [Windows 7 desarrolladores](../win7devguide/windows-7-developer-guide.md)de .

 

## <a name="thread-priorities"></a>Prioridades de subprocesos

MMCSS aumenta la prioridad de los subprocesos que trabajan en tareas multimedia de alta prioridad.

MMCSS determina la prioridad de un subproceso mediante los siguientes factores:

-   Prioridad base de la tarea.
-   Parámetro *Priority* de la [**función AvSetMmThreadPriority.**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)
-   Si la aplicación está en primer plano.
-   Cuánto tiempo de CPU consumen los subprocesos de cada categoría.

MMCSS establece la prioridad de los subprocesos de cliente en función de su categoría de programación.

| Category | Prioridad | Descripción                                                                                                                               |
|----------|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Alto     | 23-26    | Estos subprocesos se ejecutan con una prioridad de subproceso inferior a solo determinadas tareas de nivel del sistema. Esta categoría está diseñada para tareas Pro audio. |
| Media   | 16-22    | Estos subprocesos forman parte de la aplicación que está en primer plano.                                                                      |
| Bajo      | 8-15     | Esta categoría contiene el resto de los subprocesos. Se garantiza un porcentaje mínimo de los recursos de CPU si es necesario.           |
|          | 1-7      | Estos subprocesos han usado su cuota de recursos de CPU. Pueden seguir ejecándose si no hay subprocesos de prioridad baja listos para ejecutarse.                |



 

 

 
