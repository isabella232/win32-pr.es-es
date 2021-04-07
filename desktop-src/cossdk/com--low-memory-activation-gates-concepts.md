---
description: COM+ intenta evitar situaciones en las que se deben ejecutar estas rutas de acceso de error en un servidor.
ms.assetid: 0de125a2-2e91-49b9-a903-6c2e173e22a2
title: Conceptos de las puertas de activación de Low-Memory COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d844a0492301ef067f5b3cd0e0749ec3a21779
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104003269"
---
# <a name="com-low-memory-activation-gates-concepts"></a>Conceptos de las puertas de activación de Low-Memory COM+

Por lo general, la sincronización no es necesaria cuando se tiene un contenedor uniproceso (STA) porque el apartamento proporciona la sincronización automáticamente. La sincronización es importante cuando tiene un contenedor multiproceso (MTA) y un objeto de subproceso libre. En el pasado, los objetos de subprocesamiento libre tenían que controlar el bloqueo. Puede eliminar la necesidad de usar el bloqueo estableciendo el atributo de sincronización de un componente.

Los problemas de confiabilidad suelen producirse cuando los recursos de un servidor no pueden reaccionar de forma eficaz a las cargas máximas. Cuando un servidor no tiene suficientes recursos físicos para satisfacer la demanda máxima, puede agotar la memoria virtual. Esto se convierte en un problema si el código del usuario o del sistema no controla correctamente los errores de asignación de memoria. El servidor comienza a ralentizarse y, a medida que se agota la memoria, se produce un error en las asignaciones de memoria. El servidor ejecuta las rutas de acceso de error para controlar los errores de asignación. Si una ruta de acceso de error contiene un error en el código del sistema o del usuario que se ejecuta en el servidor, es muy difícil interceptar y controlar de forma segura.

COM+ intenta evitar situaciones en las que se deben ejecutar estas rutas de acceso de error en un servidor. A través de la característica de puertas de activación de memoria insuficiente, COM+ supervisa proactivamente la carga de memoria en el sistema y garantiza que haya una cantidad razonable de memoria disponible antes de ejecutar el código de usuario. Si el porcentaje de memoria virtual disponible para la aplicación cae por debajo de un umbral fijo, se produce un error en la activación antes de que se cree un objeto o una aplicación de servidor COM+ (como se muestra en la ilustración siguiente). Si se producen errores en estas activaciones que normalmente se ejecutarían, la característica de puertas de activación de memoria insuficiente minimiza los problemas asociados a las asignaciones de memoria en el código de usuario, lo que mejora considerablemente la confiabilidad del sistema.

![Diagrama que muestra la relación entre una aplicación COM+ y una puerta de activación de memoria insuficiente.](images/ada5ef02-f2b1-46bb-b0fc-fe7d65f31b43.png)

La característica de puertas de activación de memoria insuficiente solo se aplica a los componentes COM configurados que se instalan en una aplicación COM+.

## <a name="how-the-low-memory-activation-gates-feature-works"></a>Cómo funciona la característica de puertas de activación de Low-Memory

La característica de puertas de activación de memoria insuficiente usa un nivel de umbral fijo diferente en función del tipo de activación. Al crear una aplicación de servidor COM+, COM+ permite la activación si está disponible más del 10 por ciento de la memoria virtual. Si hay disponible menos del 10 por ciento, COM+ realiza una asignación de prueba para averiguar si el archivo de paginación se puede expandir para acomodar la nueva carga de memoria. Si el archivo de paginación se expande, se crea la aplicación de servidor. Si no se puede expandir el archivo de paginación, se produce un error en la activación y no se asigna la memoria.

El proceso es similar al crear un objeto. En este caso, COM+ permite la activación si está disponible más del 5 por ciento de la memoria virtual. Si hay disponible menos del 5 por ciento, COM+ continúa con una asignación de prueba. De nuevo, si la asignación de prueba expande el archivo de paginación, se crea el objeto. En caso contrario, se produce un error en la activación.

Los niveles de umbral fijos para las puertas de activación de memoria insuficiente no se pueden configurar actualmente. Por esta razón, no hay ninguna tarea asociada a esta característica.

 

 



