---
description: COM+ intenta evitar situaciones en las que estas rutas de acceso de error deben ejecutarse en un servidor.
ms.assetid: 0de125a2-2e91-49b9-a903-6c2e173e22a2
title: Conceptos de com+ Low-Memory puertas de activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b4c34e10dcb18a88566d1bc45bb6751e500767c34a2e17cf8cdf12f0f1930c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129187"
---
# <a name="com-low-memory-activation-gates-concepts"></a>Conceptos de com+ Low-Memory puertas de activación

Por lo general, la sincronización no es necesaria cuando se tiene un apartamento de un solo subproceso (STA) porque el apartamento proporciona la sincronización automáticamente. La sincronización es importante cuando tiene un apartamento multiproceso (MTA) y un objeto de subproceso libre. En el pasado, los objetos sin subprocesos tenían que controlar el bloqueo. Puede eliminar la necesidad de usar el bloqueo estableciendo el atributo de sincronización para un componente.

Los problemas de confiabilidad suelen producirse cuando los recursos de un servidor no pueden reaccionar de forma eficaz a las cargas máximas. Cuando un servidor no tiene suficientes recursos físicos para satisfacer la demanda máxima, puede agotar la memoria virtual. Esto se convierte en un problema si el código de usuario o el código del sistema no controla correctamente los errores de asignación de memoria. El servidor comienza a ralentizarse y, a medida que se agota la memoria, se producirá un error en las asignaciones de memoria. El servidor ejecuta rutas de acceso de error para controlar los errores de asignación. Si una ruta de acceso de error contiene un error en el sistema o el código de usuario que se ejecuta en el servidor, es muy difícil capturar y controlar de forma segura.

COM+ intenta evitar situaciones en las que estas rutas de acceso de error deben ejecutarse en un servidor. A través de la característica puertas de activación de memoria baja, COM+ supervisa de forma proactiva la carga de memoria en el sistema y garantiza que hay disponible una cantidad razonable de memoria antes de ejecutar el código de usuario. Si el porcentaje de memoria virtual disponible para la aplicación está por debajo de un umbral fijo, se produce un error en la activación antes de crear una aplicación o un objeto de servidor COM+ (como se muestra en la ilustración siguiente). Al dar error a estas activaciones que normalmente se ejecutarían, la característica puertas de activación de memoria baja minimiza los problemas asociados con las asignaciones de memoria en el código de usuario, lo que mejora significativamente la confiabilidad del sistema.

![Diagrama que muestra la relación entre una aplicación COM+ y una puerta de activación de memoria baja.](images/ada5ef02-f2b1-46bb-b0fc-fe7d65f31b43.png)

La característica puertas de activación de memoria baja solo se aplica a los componentes COM configurados que están instalados en una aplicación COM+.

## <a name="how-the-low-memory-activation-gates-feature-works"></a>Funcionamiento de la Low-Memory puertas de activación

La característica puertas de activación de memoria baja usa un nivel de umbral fijo diferente en función del tipo de activación. Al crear una aplicación de servidor COM+, COM+ permite la activación si hay más del 10 % de memoria virtual disponible. Si hay menos del 10 por ciento disponible, COM+ realiza una asignación de prueba para averiguar si el archivo de paginación puede expandirse para dar cabida a la nueva carga de memoria. Si el archivo de paginación se expande, se crea la aplicación de servidor. Si no se puede expandir el archivo de paginación, se produce un error en la activación y no se asigna memoria.

El proceso es similar al crear un objeto . En este caso, COM+ permite la activación si hay más del 5 % de memoria virtual disponible. Si hay disponible menos del 5 %, COM+ continúa con una asignación de prueba. De nuevo, si la asignación de prueba expande el archivo de paginación, se crea el objeto . Si no es así, se produce un error en la activación.

Los niveles de umbral fijos para las puertas de activación de memoria baja no se pueden configurar actualmente. Por esta razón, no hay ninguna tarea asociada a esta característica.

 

 



