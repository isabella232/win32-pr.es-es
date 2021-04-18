---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 2 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Tipo de acción personalizada 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0497b2a76dc2fac7f5e56f7347b50deac867757f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652890"
---
# <a name="custom-action-type-2"></a>Tipo de acción personalizada 2

Esta acción personalizada llama a un ejecutable iniciado con una línea de comandos.

## <a name="source"></a>Source

El ejecutable se genera a partir de una secuencia binaria temporal. El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla binaria](binary-table.md). La columna de datos de la tabla binaria contiene los datos de la secuencia. Se asigna una secuencia independiente para cada fila.

Se pueden insertar nuevos datos binarios de un archivo mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la tabla. Cuando se invoca la acción personalizada, los datos de la secuencia se copian en un archivo temporal, que se procesa en función del tipo de acción personalizada.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |



 

## <a name="target"></a>Destino

La columna de destino de la [tabla CustomAction](customaction-table.md) contiene la cadena de línea de comandos para el ejecutable denominado en la columna de origen.

## <a name="return-processing-options"></a>Opciones de procesamiento de valores devueltos

Incluya bits de marca opcionales en la columna tipo de la tabla CustomAction para especificar las opciones de procesamiento de valores devueltos. Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya los bits de marca opcionales en la columna tipo de la tabla CustomAction para especificar las opciones de programación de la ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opciones de ejecución de In-Script

Incluya bits de marca opcionales en la columna tipo de la tabla CustomAction para especificar una opción de ejecución en el script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente. El instalador interpreta cualquier otro valor devuelto como error. Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la tabla CustomAction.

## <a name="remarks"></a>Observaciones

Una acción personalizada que inicia un ejecutable toma una línea de comandos, que normalmente contiene las propiedades que se designan dinámicamente. Si esta es también una [acción personalizada de ejecución aplazada](deferred-execution-custom-actions.md), el instalador usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para crear el proceso cuando se invoca la acción personalizada desde el script de instalación.

Cuando se exporta una tabla de base de datos, cada secuencia se escribe como un archivo independiente en la subcarpeta con el nombre de la tabla, utilizando la clave principal como el nombre de archivo (columna Name de la tabla binaria), con una extensión predeterminada de ". ibd". El nombre debe usar el formato 8,3 si el sistema de archivos o el sistema de control de versiones no admiten nombres de archivo largos. El archivo de almacenamiento persistente reemplaza los datos de la secuencia por el nombre de archivo usado, de modo que los datos se pueden encontrar al importar la tabla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_Acciones personalizadas](custom-actions.md)
</dt> <dt>

[Archivos ejecutables](executable-files.md)
</dt> </dl>

 

 
