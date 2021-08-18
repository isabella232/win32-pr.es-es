---
description: Los desarrolladores Windows paquetes del instalador pueden optar por usar una acción personalizada de tipo 21 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: Tipo de acción personalizada 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6184455b15b1bcea1c53532ef53ef526b7af159d81322994220186d6cd187e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105265"
---
# <a name="custom-action-type-21"></a>Tipo de acción personalizada 21

Esta acción personalizada se escribe en JScript, como ECMA 262. Windows El instalador no admite JScript 1.0. Para obtener más información, vea [Scripts](scripts.md).

## <a name="source"></a>Source

El script se instala con la aplicación durante la sesión actual. El campo Source de la [tabla CustomAction contiene](customaction-table.md) una clave para la [tabla File](file-table.md). La ubicación del código de acción personalizado viene determinada por la resolución de la ruta de acceso de destino para este archivo; Por lo tanto, se debe llamar a esta acción personalizada una vez instalado el archivo y antes de quitarlo.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.



| Constantes                                                              | Hexadecimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile** | 0x015       | 21      |



 

Windows El instalador puede usar acciones personalizadas de [64 bits](64-bit-custom-actions.md) en sistemas operativos de 64 bits. Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico. Para obtener información, vea Acciones personalizadas de 64 bits. Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.



| Constantes                                                                                                     | Hexadecimal | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript** | 0x0001015   | 4117    |



 

## <a name="target"></a>Destino

El campo Target de la [tabla CustomAction contiene](customaction-table.md) una función de script opcional. El procesamiento envía primero el script para analizarlo y, a continuación, llama a la función de script opcional.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de devolución. Para obtener una descripción de las opciones y los valores, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Las funciones opcionales escritas en script deben devolver uno de los valores descritos en Valores devueltos de [JScript y Acciones personalizadas de VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).

## <a name="remarks"></a>Comentarios

Una acción personalizada escrita en JScript o VBScript requiere el objeto [**Session de**](session-object.md) instalación. El instalador asocia el **objeto de sesión** al script con el nombre "Session". Dado que es posible que el objeto **Session** no exista durante una reversión de la instalación, una acción [](obtaining-context-information-for-deferred-execution-custom-actions.md) personalizada diferida escrita en script debe usar uno de los métodos o propiedades del objeto **Session** descritos en la sección Obtención de información de contexto para acciones personalizadas de ejecución aplazada para recuperar su contexto.

Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como Custom Action Type 21 (JScript), deben cumplir las siguientes restricciones de secuenciación:

-   La acción personalizada debe secuenciarse después de [la acción CostFinalize](costfinalize-action.md). Esto es para que la acción personalizada pueda resolver la ruta de acceso necesaria para buscar el archivo de origen que contiene el JScript.
-   Si el archivo de origen aún no está instalado en el equipo, las acciones personalizadas diferidas (en script) de este tipo deben secuenciarse después de la acción [InstallFiles](installfiles-action.md).
-   Si el archivo de origen aún no está instalado en el equipo, las acciones personalizadas no diferidas de este tipo deben secuenciarse después de la [acción InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 



