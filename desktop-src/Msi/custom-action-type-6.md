---
description: Los desarrolladores Windows paquetes del instalador pueden optar por usar un tipo de acción personalizado 6 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: Tipo de acción personalizada 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd672fc9d66b5b36f31d80da06400cf27fb7f43c2f384e88bc20a7614732d87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926985"
---
# <a name="custom-action-type-6"></a>Tipo de acción personalizada 6

Esta acción personalizada se escribe en VBScript. Para obtener más información, vea [Scripts](scripts.md).

## <a name="source"></a>Source

El script se genera a partir de una secuencia binaria temporal. El campo Source de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla Binaria.](binary-table.md) La columna Datos de la tabla Binaria contiene los datos de flujo. Se asigna una secuencia independiente para cada fila.

Se pueden insertar nuevos datos binarios desde un archivo mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la tabla. Cuando se invoca la acción personalizada, los datos de flujo se copian en un archivo temporal, que luego se procesa en función del tipo de acción personalizada.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.



| Constantes                                                               | Hexadecimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData** | 0x006       | 6       |



 

Windows El instalador puede usar acciones personalizadas de 64 bits en sistemas operativos de 64 bits. Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico. Para obtener información, [vea Acciones personalizadas de 64 bits.](64-bit-custom-actions.md) Incluya el siguiente valor en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.



| Constantes                                                                                                      | Hexadecimal | Decimal |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript** | 0x0001006   | 4102    |



 

## <a name="target"></a>Destino

El campo Target de la [tabla CustomAction contiene](customaction-table.md) una función de script opcional. El procesamiento envía primero el script para su análisis y, a continuación, llama a la función de script opcional.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de devolución. Para obtener una descripción de las opciones y los valores, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Opciones de programación de ejecución de acciones personalizadas.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script de ejecución

Incluya bits de marca opcionales en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Las funciones opcionales escritas en script deben devolver uno de los valores descritos en Valores devueltos [de JScript y Acciones personalizadas de VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).

## <a name="remarks"></a>Comentarios

Una acción personalizada escrita en JScript o VBScript requiere la instalación del [**objeto session**](session-object.md). El instalador asocia el objeto **Session** al script con el nombre *Session*. Dado que es posible que el objeto **Session** no exista durante una reversión de la instalación, una acción personalizada diferida escrita en script debe usar uno de los métodos o propiedades del objeto **Session** descrito en la sección [Obtención](obtaining-context-information-for-deferred-execution-custom-actions.md) de información de contexto para acciones personalizadas de ejecución diferida para recuperar su contexto.

Cuando se exporta una tabla de base de datos, cada secuencia se escribe como un archivo independiente en la subcarpeta denominada después de la tabla, usando la clave principal como nombre de archivo (columna Nombre de la tabla binaria), con una extensión predeterminada de ".ibd". El nombre debe usar el formato de nombre de archivo 8.3 si el sistema de archivos o el sistema de control de versiones no admite nombres de archivo largos. El archivo de archivo persistente reemplaza los datos de secuencia por el nombre de archivo utilizado, de modo que los datos se puedan encontrar cuando se importe la tabla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 



