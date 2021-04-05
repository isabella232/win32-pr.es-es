---
description: El instalador ejecuta la secuencia del Asistente para la instalación de ejemplo solo si se usa el nivel de interfaz de usuario completo para instalar la aplicación.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Agregar un evento de control al final de la instalación para ejecutar el inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001763"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a>Agregar un evento de control al final de la instalación para ejecutar el inicio

El instalador ejecuta la secuencia del Asistente para la instalación de ejemplo solo si se usa el nivel de [*interfaz de usuario completo*](f-gly.md) para instalar la aplicación. El último cuadro de diálogo de la secuencia de diálogo de ejemplo es un cuadro de [diálogo de salida](exit-dialog.md) denominado ExitDialog. Cuando un usuario interactúa con el botón Aceptar en ExitDialog, primero publica un [ControlEvent, EndDialog](enddialog-controlevent.md) que devuelve el control al instalador. Después, el control publica una [ControlEvent, de acción](doaction-controlevent.md) que ejecuta la acción personalizada Launch. Cada evento de control requiere un registro en la [tabla ControlEvent,](controlevent-table.md). Consulte [información general de ControlEvent,](controlevent-overview.md).

[Tabla ControlEvent,](controlevent-table.md)



| Diálogo     | control\_ | Evento     | Argumento | Condición                     | Ordenación |
|------------|-----------|-----------|----------|-------------------------------|----------|
| ExitDialog | Aceptar        | EndDialog | Valor devuelto   | 1                             | 1        |
| ExitDialog | Aceptar        | DoAction  | Launch   | NO instalado y $Tutorial = 3 | 2        |



 

La condición en el control de la acción garantiza que la acción personalizada se ejecute solo durante la primera instalación de la aplicación y que se instale localmente. La frase $Tutorial = 3 significa que el estado de acción del componente tutorial está establecido en local. Consulte [Sintaxis de la instrucción condicional](conditional-statement-syntax.md).

Esto completa el ejemplo.

 

 



