---
description: Los desarrolladores de Windows Installer pueden optar por usar un tipo de acción personalizado 2 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Tipo de acción personalizada 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba648578ecdd9d300a5cf15793e3abd9407f78853830f49c16a26db184ff3683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996855"
---
# <a name="custom-action-type-2"></a>Tipo de acción personalizada 2

Esta acción personalizada llama a un ejecutable iniciado con una línea de comandos.

## <a name="source"></a>Origen

El archivo ejecutable se genera a partir de una secuencia binaria temporal. El campo Source de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla Binaria.](binary-table.md) La columna Datos de la tabla Binaria contiene los datos de flujo. Se asigna una secuencia independiente para cada fila.

Se pueden insertar nuevos datos binarios desde un archivo mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la tabla. Cuando se invoca la acción personalizada, los datos de flujo se copian en un archivo temporal, que luego se procesa en función del tipo de acción personalizada.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |



 

## <a name="target"></a>Destino

La columna Target de la [tabla CustomAction contiene](customaction-table.md) la cadena de línea de comandos para el ejecutable denominado en la columna Source.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Incluya bits de marca opcionales en la columna Tipo de la tabla CustomAction para especificar las opciones de procesamiento de devolución. Para obtener una descripción de las opciones y los valores, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la tabla CustomAction para especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Opciones de programación de ejecución de acciones personalizadas.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script de ejecución

Incluya bits de marca opcionales en la columna Type de la tabla CustomAction para especificar una opción de ejecución en script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente. El instalador interpreta cualquier otro valor devuelto como error. Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Tipo de la tabla CustomAction.

## <a name="remarks"></a>Comentarios

Una acción personalizada que inicia un ejecutable toma una línea de comandos, que normalmente contiene propiedades designadas dinámicamente. Si también se trata [de](deferred-execution-custom-actions.md)una acción personalizada de ejecución aplazada, el instalador usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para crear el proceso cuando se invoca la acción personalizada desde el script de instalación.

Cuando se exporta una tabla de base de datos, cada secuencia se escribe como un archivo independiente en la subcarpeta denominada después de la tabla, usando la clave principal como nombre de archivo (columna Nombre de la tabla binaria), con una extensión predeterminada de ".ibd". El nombre debe usar el formato 8.3 si el sistema de archivos o el sistema de control de versiones no admite nombres de archivo largos. El archivo de archivo persistente reemplaza los datos de secuencia por el nombre de archivo utilizado, de modo que los datos se puedan encontrar cuando se importe la tabla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> <dt>

[Archivos ejecutables](executable-files.md)
</dt> </dl>

 

 
