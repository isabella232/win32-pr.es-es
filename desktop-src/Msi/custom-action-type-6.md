---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 6 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: Tipo de acción personalizada 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652838"
---
# <a name="custom-action-type-6"></a>Tipo de acción personalizada 6

Esta acción personalizada se escribe en VBScript. Para obtener más información, vea [scripts](scripts.md).

## <a name="source"></a>Source

El script se genera a partir de una secuencia binaria temporal. El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla binaria](binary-table.md). La columna de datos de la tabla binaria contiene los datos de la secuencia. Se asigna una secuencia independiente para cada fila.

Se pueden insertar nuevos datos binarios de un archivo mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la tabla. Cuando se invoca la acción personalizada, los datos de la secuencia se copian en un archivo temporal, que se procesa en función del tipo de acción personalizada.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.



| Constantes                                                               | Hexadecimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData** | 0x006       | 6       |



 

Windows Installer puede usar las acciones personalizadas de 64 bits en sistemas operativos de 64 bits. Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico. Para obtener información, consulte [acciones personalizadas de 64 bits](64-bit-custom-actions.md). Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.



| Constantes                                                                                                      | Hexadecimal | Decimal |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript** | 0x0001006   | 4102    |



 

## <a name="target"></a>Destino

El campo de destino de la [tabla CustomAction](customaction-table.md) contiene una función de script opcional. El procesamiento primero envía el script para el análisis y, a continuación, llama a la función de script opcional.

## <a name="return-processing-options"></a>Opciones de procesamiento de valores devueltos

Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos. Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opciones de ejecución de In-Script

Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Las funciones opcionales escritas en el script deben devolver uno de los valores descritos en [valores devueltos de las acciones personalizadas de JScript y VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).

## <a name="remarks"></a>Observaciones

Una acción personalizada escrita en JScript o VBScript requiere la instalación del [**objeto de sesión**](session-object.md). El instalador adjunta el objeto de **sesión** al script con la *sesión* de nombre. Dado que es posible que el objeto de **sesión** no exista durante una reversión de la instalación, una acción personalizada diferida escrita en el script debe usar uno de los métodos o propiedades del objeto de **sesión** que se describe en la sección [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar su contexto.

Cuando se exporta una tabla de base de datos, cada secuencia se escribe como un archivo independiente en la subcarpeta con el nombre de la tabla, utilizando la clave principal como el nombre de archivo (columna Name de la tabla binaria), con una extensión predeterminada de ". ibd". El nombre debe usar el formato de nombre de archivo 8,3 si el sistema de archivos o el sistema de control de versiones no admiten nombres de archivo largos. El archivo de almacenamiento persistente reemplaza los datos de la secuencia por el nombre de archivo usado, de modo que los datos se pueden encontrar al importar la tabla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_Acciones personalizadas](custom-actions.md)
</dt> </dl>

 

 



