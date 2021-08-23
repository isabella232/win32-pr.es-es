---
description: Los conjuntos de CPU proporcionan API para declarar la afinidad de la aplicación de forma "flexible" compatible con la administración de energía del sistema operativo.
ms.assetid: FF8BE790-19D9-473F-B184-C54FB392D61A
title: Conjuntos de CPU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 092559fbf5646a0938696c953f4136f1fe1a9567e56e02a04c6c36510d03d729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143128"
---
# <a name="cpu-sets"></a>Conjuntos de CPU

Los conjuntos de CPU proporcionan API para declarar la afinidad de la aplicación de forma "flexible" compatible con la administración de energía del sistema operativo. Además, la API proporciona a las aplicaciones la capacidad de reinicializar todos los subprocesos en segundo plano del proceso a un subconjunto de procesadores mediante el mecanismo Process **Default** para evitar interferencias de subprocesos del sistema operativo dentro del proceso. Algunas versiones de Windows admiten directivas de reserva básica, en las que un subconjunto de los conjuntos de CPU del sistema se puede dedicar al uso exclusivo de aplicaciones y cargas de trabajo individuales.

La API de conjunto de CPU funciona con los ID de conjunto de CPU, que están asociados a afinidades de procesador virtual. En la mayoría de los sistemas y en la mayoría de las condiciones, cada identificador de conjunto de CPU se asignará directamente a un **único** procesador lógico principal. Normalmente, un subproceso con afinidad con un conjunto de CPU determinado se ejecutará en uno de los procesadores de su lista de los ID de conjunto de CPU seleccionados.

Los conjuntos de CPU reservados se pueden determinar inspeccionando la marca **Asignado** en SYSTEM \_ CPU SET \_ \_ INFORMATION. El sistema controla el acceso a los conjuntos de CPU reservados y la asignación se puede consultar mediante la **marca AllocatedToTargetProcess** de la estructura SYSTEM \_ CPU SET \_ \_ INFORMATION. Si un proceso intenta usar una asignación de conjunto de CPU que se asigna exclusivamente a otros procesos, su solicitud se omite y los subprocesos asignados a conjuntos de CPU no permitidos se programan en otro lugar. Los conjuntos de CPU se pueden asignar en dos niveles. Los conjuntos de CPU Process Default se asignan a todos los subprocesos de un proceso que no tienen una asignación en el nivel De subproceso seleccionado. Si un subproceso o proceso tiene un conjunto restrictivo de máscara de afinidad, la máscara de afinidad se respeta por encima de cualquier asignación de conjunto de CPU en conflicto. En sistemas de varios grupos, las asignaciones de CPU se omiten si se encuentran en grupos que no coinciden con el grupo de la máscara de afinidad del subproceso. Si un subproceso se asigna a varios conjuntos de CPU válidos, se ejecutará en uno de los procesadores correspondientes según sus prioridades y las prioridades de los subprocesos de la competencia en esos procesadores.

**Funciones, enumeraciones y estructuras del conjunto de CPU**

-   [**Función GetProcessDefaultCpuSets**](getprocessdefaultcpusets.md)
-   [**Función GetSystemCpuSetInformation**](getsystemcpusetinformation.md)
-   [**Función GetThreadSelectedCpuSets**](getthreadselectedcpusets.md)
-   [**Función SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md)
-   [**Función SetThreadSelectedCpuSets**](setthreadselectedcpusets.md)
-   [**CPU \_ Enumeración SET \_ INFORMATION \_ TYPE**](cpu-set-information-type.md)
-   [**SYSTEM \_ ESTRUCTURA DE \_ INFORMACIÓN \_ DEL CONJUNTO DE CPU**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

 

 



