---
description: Los desarrolladores de Windows Installer pueden optar por usar un tipo de acción personalizado 34 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Tipo de acción personalizada 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158692"
---
# <a name="custom-action-type-34"></a>Tipo de acción personalizada 34

Esta acción personalizada llama a un ejecutable iniciado con una línea de comandos. Para obtener más información, vea [Archivos ejecutables](executable-files.md).

## <a name="source"></a>Source

El archivo ejecutable se genera a partir de un archivo. El campo Source de la [tabla CustomAction](customaction-table.md) contiene una clave en la [tabla Directory.](directory-table.md) La entrada de tabla Directory a la que se hace referencia se usa para resolver la ruta de acceso completa a un directorio de trabajo. No es necesario que sea la ruta de acceso al directorio que contiene el archivo ejecutable.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                         | Hexadecimal | Decimal |
|-------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeDirectory** | 0x022       | 34      |



 

## <a name="target"></a>Destino

La columna Target de la [tabla CustomAction](customaction-table.md) contiene la ruta de acceso completa y el nombre del archivo ejecutable seguidos de argumentos opcionales para el ejecutable. Se requiere la ruta de acceso completa y el nombre del archivo ejecutable. Las comillas deben usarse en torno a rutas de acceso o nombres de archivo largos. El valor se trata como [texto](formatted.md) con formato y puede contener referencias a propiedades, archivos, directorios u otros atributos de texto con formato.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de devolución. Para obtener una descripción de las opciones y los valores, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Opciones de programación de ejecución de acciones personalizadas.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script de ejecución

Incluya bits de marca opcionales en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente. El instalador interpreta cualquier otro valor devuelto como error. Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la [tabla CustomAction.](customaction-table.md)

## <a name="remarks"></a>Observaciones

Una acción personalizada que inicia un ejecutable toma una línea de comandos, que normalmente contiene propiedades designadas dinámicamente. Si también se trata [de](deferred-execution-custom-actions.md)una acción personalizada de ejecución aplazada, el instalador usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para crear el proceso cuando se invoca la acción personalizada desde el script de instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 
