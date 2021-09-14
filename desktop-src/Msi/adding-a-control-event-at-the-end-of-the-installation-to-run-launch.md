---
description: El instalador ejecuta la secuencia del asistente de instalación del ejemplo solo si se usa el nivel de interfaz de usuario completo para instalar la aplicación.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Agregar un evento de control al final de la instalación para ejecutar el inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159223"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a>Agregar un evento de control al final de la instalación para ejecutar el inicio

El instalador ejecuta la secuencia del asistente de instalación del ejemplo solo si se usa el [*nivel de*](f-gly.md) interfaz de usuario completo para instalar la aplicación. El último cuadro de diálogo de la secuencia de diálogo de ejemplo es [un cuadro de diálogo de salida](exit-dialog.md) denominado ExitDialog. Cuando un usuario interactúa con el botón Aceptar en ExitDialog, publica por primera vez [un control EndDialog ControlEvent](enddialog-controlevent.md) que devuelve el control al instalador. A continuación, el control publica un [control ControlEvent de DoAction](doaction-controlevent.md) que ejecuta la acción personalizada Launch. Cada evento de control requiere un registro en la [tabla ControlEvent](controlevent-table.md). Consulte [Información general de ControlEvent.](controlevent-overview.md)

[Tabla ControlEvent](controlevent-table.md)



| Diálogo     | control\_ | Evento     | Argumento | Condición                     | Ordenación |
|------------|-----------|-----------|----------|-------------------------------|----------|
| ExitDialog | Aceptar        | EndDialog | Valor devuelto   | 1                             | 1        |
| ExitDialog | Aceptar        | DoAction  | Launch   | NOT Installed AND $Tutorial=3 | 2        |



 

La condición del control DoAction garantiza que la acción personalizada solo se ejecuta durante la primera instalación de la aplicación y que se instala localmente. La frase $Tutorial=3 significa que el estado de acción del componente Tutorial está establecido en local. Vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

Esto completa el ejemplo.

 

 



