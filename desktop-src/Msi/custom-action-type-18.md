---
description: Los desarrolladores de Windows Installer pueden optar por usar un tipo de acción personalizada 18 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Tipo de acción personalizada 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a669fe3caa532b3a365f1056ca2b36f490ab95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158704"
---
# <a name="custom-action-type-18"></a>Tipo de acción personalizada 18

Esta acción personalizada llama a un ejecutable iniciado con una línea de comandos.

## <a name="source"></a>Source

El archivo ejecutable se genera a partir de un archivo instalado con la aplicación. El campo Source de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla File](file-table.md). La ubicación del código de acción personalizada viene determinada por la resolución de la ruta de acceso de destino para este archivo; Por lo tanto, se debe llamar a esta acción personalizada una vez instalado el archivo y antes de quitarlo.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |



 

## <a name="target"></a>Destino

La columna Target de la [tabla CustomAction contiene](customaction-table.md) la cadena de línea de comandos para el ejecutable identificado en la columna Source.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de devolución. Para obtener una descripción de las opciones y los valores, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Opciones de programación de ejecución de acciones personalizadas.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script de ejecución

Incluya bits de marca opcionales en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente. El instalador interpreta cualquier otro valor devuelto como error. Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Tipo de la tabla CustomAction.

## <a name="remarks"></a>Observaciones

Una acción personalizada que inicia un ejecutable toma una línea de comandos, que normalmente contiene propiedades designadas dinámicamente. Si también se trata [de](deferred-execution-custom-actions.md)una acción personalizada de ejecución aplazada, el instalador usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para crear el proceso cuando se invoca la acción personalizada desde el script de instalación.

Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como Custom Action Type 18 (EXE), deben cumplir las siguientes restricciones de secuenciación:

-   La acción personalizada debe secuenciarse después de [la acción CostFinalize](costfinalize-action.md). Esto es para que la acción personalizada pueda resolver la ruta de acceso necesaria para buscar el exe.
-   Si el archivo de origen aún no está instalado en el equipo, las acciones personalizadas diferidas (en script) de este tipo deben secuenciarse después de la [acción InstallFiles](installfiles-action.md).
-   Si el archivo de origen aún no está instalado en el equipo, las acciones personalizadas no diferidas de este tipo deben secuenciarse después de [la acción InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> <dt>

[Archivos ejecutables](executable-files.md)
</dt> </dl>

 

 
