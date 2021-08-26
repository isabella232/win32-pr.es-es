---
description: Las acciones personalizadas se programan en tablas de secuencia de la misma manera que las acciones estándar.
ms.assetid: 1aea75b1-a498-405e-9208-91672455496b
title: Secuenciación de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d86449b67809f782560e35d32b1b1e42434153ced776a27fd479a7b80a25a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039975"
---
# <a name="sequencing-custom-actions"></a>Secuenciación de acciones personalizadas

Las acciones personalizadas se programan en tablas de secuencia de la misma manera que las acciones estándar.

**Para programar una acción personalizada en una tabla de secuencia**

1.  Escriba el nombre de acción personalizada (que es la clave principal de la [tabla CustomAction)](customaction-table.md)en la columna Acción de la [tabla Sequence.](sequence-table-detailed-example.md)
2.  Escriba la secuencia de la acción personalizada con respecto a las demás acciones de la tabla en la columna Secuencia de la [tabla Secuencia.](sequence-table-detailed-example.md) Para obtener más información sobre las tablas de secuencia, vea [Usar una tabla de secuencia.](using-a-sequence-table.md)
3.  Para omitir condicionalmente la acción, escriba una expresión condicional en la columna Condición de la [tabla Sequence.](sequence-table-detailed-example.md) El instalador omite esta acción si la expresión se evalúa como FALSE.

Como en el caso de las acciones estándar, las acciones personalizadas que se programan en [InstallUISequence](installuisequence-table.md) o [AdminUISequence](adminuisequence-table.md) solo se ejecutan si la interfaz de usuario interna está establecida en el nivel completo. El nivel de interfaz de usuario se establece mediante la [**función MsiSetInternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

Las acciones estándar y personalizadas programadas en las tablas [InstallExecuteSequence,](installexecutesequence-table.md) [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) no hacen cambios en el sistema. En su lugar, el instalador pone en cola los registros de ejecución en un script para su posterior ejecución durante el servicio de instalación. Si no hay ningún servicio de instalación, las acciones programadas en estas tablas se ejecutan en el mismo contexto que la secuencia de interfaz de usuario.

Si el servidor del instalador no está registrado, las acciones personalizadas se ejecutan en el lado cliente. Si el servidor está registrado y usa el modo de interfaz de usuario completo, las acciones personalizadas se ejecutan en el lado servidor.

Si usa la interfaz de usuario completa con el servidor, las acciones iniciales anteriores a la acción [InstallValidate](installvalidate-action.md) se ejecutan en el cliente para permitir la interacción completa. A continuación, la ejecución se cambia al servidor que repite esas acciones y ejecuta las acciones de ejecución del script. Esto va seguido de una devolución al cliente para las acciones finales.

Tenga en cuenta que si se quita un producto estableciendo su característica superior en ausente, es posible que la propiedad [**REMOVE**](remove.md) no sea igual a ALL hasta después de [la acción InstallValidate.](installvalidate-action.md) Esto significa que cualquier acción personalizada que dependa de REMOVE=ALL debe secuenciarse después de la acción InstallValidate. Una acción personalizada puede comprobar REMOVE para determinar si un producto se ha establecido para que se desinstale completamente.

Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como Custom Action Type 17 (DLL), Custom Action Type 18 (EXE), Custom Action Type 21 (JScript) y Custom Action Type 22 (VBScript), deben cumplir las restricciones de secuenciación siguientes.

-   La acción personalizada debe secuenciarse después de la acción [CostFinalize](costfinalize-action.md) para que se pueda resolver la ruta de acceso al archivo al que se hace referencia.
-   Si el archivo de origen aún no está instalado en el equipo, las acciones personalizadas diferidas (en script) deben secuenciarse después de [InstallFiles](installfiles-action.md).
-   Si el archivo de origen aún no está instalado en el equipo, las acciones personalizadas no deducidas deben secuenciarse después de [la acción InstallInitialize.](installinitialize-action.md)

Las siguientes restricciones de secuenciación se aplican a las acciones personalizadas que cambian o actualizan un paquete Windows Installer.

-   Si la acción personalizada cambia el paquete, por ejemplo agregando filas a una tabla, la acción debe secuenciarse antes de [la acción InstallInitialize.](installinitialize-action.md)
-   Si la acción personalizada realiza cambios que afectarían al costo, se debe secuenciar antes de la [acción CostInitialize.](costfinalize-action.md)
-   Si la acción personalizada cambia el estado de instalación de características o componentes, se debe secuenciar antes de [la acción InstallValidate.](installvalidate-action.md)

 

 



