---
description: Los conjuntos de CPU proporcionan API para declarar la afinidad de la aplicación de forma "soft" que es compatible con la administración de energía del sistema operativo.
ms.assetid: FF8BE790-19D9-473F-B184-C54FB392D61A
title: Conjuntos de CPU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801474591751f04a5bffe570d6b8caff4974203f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677866"
---
# <a name="cpu-sets"></a>Conjuntos de CPU

Los conjuntos de CPU proporcionan API para declarar la afinidad de la aplicación de forma "soft" que es compatible con la administración de energía del sistema operativo. Además, la API proporciona a las aplicaciones la capacidad de reaffinitize todos los subprocesos en segundo plano del proceso a un subconjunto de procesadores mediante el mecanismo **predeterminado del proceso** para evitar interferencias de subprocesos del sistema operativo dentro del proceso. Algunas versiones de Windows admiten directivas de reserva principales, en las que un subconjunto de los conjuntos de CPU del sistema se puede dedicar al uso exclusivo de aplicaciones y cargas de trabajo individuales.

La API del conjunto de CPU funciona con los identificadores de conjuntos de CPU, que están asociados a las afinidades de procesador virtual. En la mayoría de los sistemas, y en la mayoría de las condiciones, cada identificador de conjunto de CPU se asignará directamente a un solo procesador lógico de **Inicio** . Un subproceso afinidad con a un conjunto de CPU determinado normalmente se ejecutará en uno de los procesadores de su lista de identificadores de conjunto de CPU seleccionados.

Los conjuntos de CPU que se reservan se pueden determinar mediante la inspección de la marca **asignada** en la información del conjunto de CPU del sistema \_ \_ \_ . El sistema controla el acceso a los conjuntos de CPU reservados y la asignación se puede consultar mediante la marca **AllocatedToTargetProcess** de la estructura de información de conjunto de CPU del sistema \_ \_ \_ . Si un proceso intenta utilizar una asignación de conjunto de CPU que se asigna exclusivamente a otros procesos, se omite su solicitud y se programan los subprocesos asignados a los conjuntos de CPU no permitidos en otra parte. Los conjuntos de CPU se pueden asignar en dos niveles. Los conjuntos de CPU predeterminados del proceso se asignan a todos los subprocesos de un proceso que no tienen una asignación en el nivel seleccionado del subproceso. Si un subproceso o proceso tiene un conjunto de máscara de afinidad restrictiva, la máscara de afinidad se respeta sobre cualquier asignación de conjunto de CPU en conflicto. En sistemas de varios grupos, las asignaciones de CPU se omiten si se encuentran en grupos que no coinciden con el grupo de la máscara de afinidad del subproceso. Si un subproceso se asigna a varios conjuntos de CPU válidos, se ejecutará en uno de los procesadores correspondientes según sus prioridades y las prioridades de los subprocesos de la competencia en esos procesadores.

**Funciones, enumeraciones y estructuras de conjunto de CPU**

-   [**GetProcessDefaultCpuSets**](getprocessdefaultcpusets.md) función)
-   [**GetSystemCpuSetInformation**](getsystemcpusetinformation.md) función)
-   [**GetThreadSelectedCpuSets**](getthreadselectedcpusets.md) función)
-   [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md) función)
-   [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) función)
-   [**CPU \_ de Enumeración de \_ \_ tipo de información Set**](cpu-set-information-type.md)
-   [**Del sistema \_ Estructura \_ de \_ información de conjunto de CPU**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

 

 



