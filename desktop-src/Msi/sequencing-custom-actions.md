---
description: Las acciones personalizadas se programan en las tablas de secuencia de la misma manera que las acciones estándar.
ms.assetid: 1aea75b1-a498-405e-9208-91672455496b
title: Secuenciar acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7c24fb91247a36880cb808c9b8e10437312cf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279323"
---
# <a name="sequencing-custom-actions"></a>Secuenciar acciones personalizadas

Las acciones personalizadas se programan en las tablas de secuencia de la misma manera que las acciones estándar.

**Para programar una acción personalizada en una tabla de secuencia**

1.  Escriba el nombre de la acción personalizada (que es la clave principal de la tabla [CustomAction](customaction-table.md)) en la columna Acción de la tabla de [secuencia](sequence-table-detailed-example.md) .
2.  Escriba la secuencia de la acción personalizada en relación con las demás acciones de la tabla en la columna secuencia de la tabla de [secuencia](sequence-table-detailed-example.md) . Para obtener más información sobre las tablas de secuencia, vea [usar una tabla de secuencia](using-a-sequence-table.md).
3.  Para omitir condicionalmente la acción, escriba una expresión condicional en la columna condición de la tabla de [secuencia](sequence-table-detailed-example.md) . El instalador omite esta acción si la expresión se evalúa como FALSE.

Como en el caso de las acciones estándar, las acciones personalizadas que se programan en [InstallUISequence](installuisequence-table.md) o [AdminUISequence](adminuisequence-table.md) solo se ejecutan si la interfaz de usuario interna está establecida en el nivel completo. El nivel de interfaz de usuario se establece mediante la función [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .

Las acciones estándar y personalizadas programadas en las tablas [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) no realizan cambios en el sistema. En su lugar, el instalador pone en cola los registros de ejecución en un script para su posterior ejecución durante el servicio de instalación. Si no hay ningún servicio de instalación, las acciones programadas en estas tablas se ejecutan en el mismo contexto que la secuencia de la interfaz de usuario.

Si el servidor del instalador no está registrado, las acciones personalizadas se ejecutan en el lado cliente. Si el servidor está registrado y usa el modo de interfaz de usuario completa, las acciones personalizadas se ejecutan en el lado del servidor.

Si usa la interfaz de usuario completa con el servidor, las acciones iniciales anteriores a la acción [InstallValidate](installvalidate-action.md) se ejecutan en el cliente para permitir una interacción completa. La ejecución se cambia al servidor, que repite las acciones y ejecuta las acciones de ejecución del script. Esto va seguido de una devolución al cliente para las acciones finales.

Tenga en cuenta que si se quita un producto al establecer su característica Top en absent, la propiedad [**Remove**](remove.md) puede no ser igual a toda hasta después de la acción [InstallValidate](installvalidate-action.md) . Esto significa que cualquier acción personalizada que dependa de REMOVE = ALL se debe secuenciar después de la acción InstallValidate. Una acción personalizada puede activar quitar para determinar si se ha configurado un producto para que se desinstale por completo.

Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como el tipo de acción personalizada 17 (DLL), el tipo de acción personalizada 18 (EXE), el tipo de acción personalizada 21 (JScript) y el tipo de acción personalizada 22 (VBScript), deben cumplir las siguientes restricciones de secuenciación.

-   La acción personalizada se debe secuenciar después de la acción [CostFinalize](costfinalize-action.md) para que se pueda resolver la ruta de acceso al archivo al que se hace referencia.
-   Si el archivo de origen todavía no está instalado en el equipo, las acciones personalizadas diferidas (en script) deben secuenciarse después de la [InstallFiles](installfiles-action.md).
-   Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas de nondeferred se deben secuenciar después de la acción [InstallInitialize](installinitialize-action.md) .

Las siguientes restricciones de secuenciación se aplican a las acciones personalizadas que cambian o actualizan un paquete de Windows Installer.

-   Si la acción personalizada cambia el paquete, por ejemplo agregando filas a una tabla, la acción se debe secuenciar antes de la acción [InstallInitialize](installinitialize-action.md) .
-   Si la acción personalizada realiza cambios que afectan a los costos, se debe secuenciar antes de la acción [CostInitialize](costfinalize-action.md) .
-   Si la acción personalizada cambia el estado de la instalación de las características o componentes, se debe secuenciar antes de la acción [InstallValidate](installvalidate-action.md) .

 

 



