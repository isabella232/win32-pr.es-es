---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 18 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Tipo de acción personalizada 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a669fe3caa532b3a365f1056ca2b36f490ab95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002926"
---
# <a name="custom-action-type-18"></a>Tipo de acción personalizada 18

Esta acción personalizada llama a un ejecutable iniciado con una línea de comandos.

## <a name="source"></a>Source

El ejecutable se genera a partir de un archivo instalado con la aplicación. El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla de archivos](file-table.md). La ubicación del código de acción personalizada viene determinada por la resolución de la ruta de acceso de destino para este archivo; por lo tanto, se debe llamar a esta acción personalizada después de haber instalado el archivo y antes de quitarlo.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |



 

## <a name="target"></a>Destino

La columna de destino de la [tabla CustomAction](customaction-table.md) contiene la cadena de línea de comandos para el ejecutable identificado en la columna de origen.

## <a name="return-processing-options"></a>Opciones de procesamiento de valores devueltos

Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos. Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opciones de ejecución de In-Script

Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente. El instalador interpreta cualquier otro valor devuelto como error. Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la tabla CustomAction.

## <a name="remarks"></a>Observaciones

Una acción personalizada que inicia un ejecutable toma una línea de comandos, que normalmente contiene las propiedades que se designan dinámicamente. Si esta es también una [acción personalizada de ejecución aplazada](deferred-execution-custom-actions.md), el instalador usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para crear el proceso cuando se invoca la acción personalizada desde el script de instalación.

Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como el tipo de acción personalizada 18 (EXE), deben cumplir las siguientes restricciones de secuenciación:

-   La acción personalizada se debe secuenciar después de la [acción CostFinalize](costfinalize-action.md). Esto es para que la acción personalizada pueda resolver la ruta de acceso necesaria para localizar el archivo EXE.
-   Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas diferidas (en script) de este tipo deben secuenciarse después de la [acción InstallFiles](installfiles-action.md).
-   Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas no diferidas de este tipo se deben secuenciar después de la [acción InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_Acciones personalizadas](custom-actions.md)
</dt> <dt>

[Archivos ejecutables](executable-files.md)
</dt> </dl>

 

 
