---
description: El costo es el proceso de determinar los requisitos de espacio total en disco para una instalación.
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: Costo de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad2dc3ad9da4fab21345e74f3f9db99992445d7cf1e2266806bda55cd6ca638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529585"
---
# <a name="file-costing"></a>Costo de archivos

El costo es el proceso de determinar los requisitos de espacio total en disco para una instalación. Los elementos calculados en el proceso de cálculo de costos de archivos incluyen la cantidad de espacio en disco en el que se instalan o quitan los archivos, así como la cantidad de espacio en disco ocupado por las entradas del Registro, los accesos directos y otros archivos varios. Los archivos existentes programados para sobrescribirse también se calculan en los totales de costo del disco.

Los costos totales se acumulan por componente y constan de tres partes independientes: costos locales, costos de origen y costos de eliminación.[](components-and-features.md) Estas partes corresponden al costo de disco en el que se incurre si el componente se instala localmente, se instala para ejecutarse desde el medio de origen o se quita.

Todos los cálculos que implican el costo de la instalación de archivos dependen del volumen de disco en el que se va a instalar o quitar el archivo. Cada vez que cambia el directorio asociado a un componente, se deben volver a calcular los costos de los archivos de instalación controlados por ese componente. Por ejemplo, dado que un cambio de directorio también puede implicar un cambio de volumen, se deben volver a calcular los tamaños de archivo en clúster. Además, se debe comprobar el nuevo directorio para determinar si se deben tener en cuenta los archivos existentes que se puedan sobrescribir.

Después de [llamar a la acción CostInitialize,](costinitialize-action.md) se debe llamar a la acción [FileCost.](filecost-action.md) La acción CostInitialize inicializa las rutinas internas del instalador que calculan dinámicamente los costos de disco implicados en las acciones de instalación estándar. En este momento no se realizan otros cálculos de costos dinámicos.

A continuación, se debe llamar a la acción [CostFinalize.](costfinalize-action.md) Esta acción finalizará todos los cálculos de costos y hará que los datos de los costos estén disponibles a través de la [tabla](component-table.md) Componente.

Una vez completada la ejecución de la acción [CostFinalize,](costfinalize-action.md) la tabla [Component](component-table.md) se inicializa completamente y se puede iniciar una secuencia de cuadro de diálogo de la interfaz de usuario que contiene un control [SelectionTree](selectiontree-control.md) si es necesario. Los cuadros de diálogo de la interfaz de usuario pueden ofrecer la opción de cambiar el estado de selección o el directorio de destino de cualquier característica de la [tabla](feature-table.md) Característica al usuario. El proceso es similar cuando cambia el estado de selección de un componente; sin embargo, en este caso, el costo dinámico del componente modificado solo se recalcula.

Una vez que el usuario haya completado la selección de características en la interfaz de usuario, se debe llamar a la acción [InstallValidate.](installvalidate-action.md) Esta acción comprueba que todos los volúmenes a los que se ha atribuido el costo tienen espacio suficiente para la instalación.

 

 



