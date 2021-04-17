---
description: El costo es el proceso de determinar los requisitos totales de espacio en disco para una instalación de.
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: Costo de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a4e6221775c2b9ecc429bd32f136e519a2b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666806"
---
# <a name="file-costing"></a>Costo de archivos

El costo es el proceso de determinar los requisitos totales de espacio en disco para una instalación de. Los elementos calculados en el proceso de cálculo de costos de archivos incluyen la cantidad de espacio en disco en el que se instalan o quitan archivos, así como la cantidad de espacio en disco que ocupan las entradas del registro, los accesos directos y otros archivos varios. Los archivos existentes programados para sobrescribirse también se calculan en los totales de costo del disco.

Los costos totales se acumulan por[componente](components-and-features.md) y se componen de tres partes independientes: costos locales, costos de origen y costos de eliminación. Estas partes se corresponden con el costo del disco que se incurre si el componente se instala localmente, se instala para ejecutarse desde el medio de origen o se quita.

Todos los cálculos que impliquen el costo de la instalación de archivos dependen del volumen de disco en el que se va a instalar o quitar el archivo. Cada vez que cambia el directorio asociado a un componente, se deben volver a calcular los costos de los archivos de instalación controlados por ese componente. Por ejemplo, dado que un cambio de directorio también puede implicar un cambio de volumen, se deben volver a calcular los tamaños de archivo en clúster. Además, se debe comprobar el nuevo directorio para determinar si se deben tener en cuenta los archivos existentes que se puedan sobrescribir.

Después de llamar a la acción [CostInitialize](costinitialize-action.md) , se debe llamar a la acción [FileCost](filecost-action.md) . La acción CostInitialize inicializa las rutinas internas del instalador que calculan dinámicamente los costos de disco implicados en las acciones de instalación estándar. No se realiza ningún otro cálculo de costos dinámicos en este momento.

A continuación, se debe llamar a la acción [CostFinalize](costfinalize-action.md) . Esta acción finaliza todos los cálculos de costos y hace que los datos de costo estén disponibles a través de la tabla de [componentes](component-table.md) .

Una vez finalizada la ejecución de la acción [CostFinalize](costfinalize-action.md) , la tabla de [componentes](component-table.md) se inicializa completamente y se puede iniciar una secuencia de cuadro de diálogo de interfaz de usuario que contiene un control [SelectionTree](selectiontree-control.md) si es necesario. Los cuadros de diálogo de la interfaz de usuario pueden ofrecer la opción de cambiar el estado de selección o el directorio de destino de cualquier característica de la tabla de [características](feature-table.md) al usuario. El proceso es similar cuando cambia el estado de selección de un componente; sin embargo, en este caso, solo se vuelve a calcular el costo dinámico del componente modificado.

Una vez que el usuario ha completado la selección de características en la interfaz de usuario, se debe llamar a la acción [InstallValidate](installvalidate-action.md) . Esta acción comprueba que todos los volúmenes a los que se ha asignado el costo tienen suficiente espacio para la instalación.

 

 



