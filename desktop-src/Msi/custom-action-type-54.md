---
description: Los desarrolladores Windows paquetes del instalador pueden optar por usar una acción personalizada de tipo 54 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Tipo de acción personalizada 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c206eec715982e1fd23978a04393b6036f77abf4c18807d2e5d43d27755640c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520085"
---
# <a name="custom-action-type-54"></a>Tipo de acción personalizada 54

Esta acción personalizada se escribe en VBScript. Vea también [Scripts](scripts.md).

## <a name="source"></a>Origen

El campo Source de la [tabla CustomAction](customaction-table.md) contiene un nombre de propiedad o una clave para la tabla [Property](property-table.md) de una propiedad que contiene el texto del script.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.



| Constantes                                                             | Hexadecimal | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty** | 0x036       | 54      |



 

Windows El instalador puede usar acciones personalizadas de 64 bits en sistemas operativos de 64 bits. Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico. Para obtener información, [vea Acciones personalizadas de 64 bits.](64-bit-custom-actions.md) Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.



| Constantes                                                                                                    | Hexadecimal | Decimal |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript** | 0x0001036   | 4150    |



 

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

Una acción personalizada escrita en JScript o VBScript requiere la instalación del [**objeto Session.**](session-object.md) El instalador asocia el objeto **de sesión** al script con el nombre *Session*. Dado que es posible que el objeto **Session** no exista durante una reversión de la instalación, una acción [](obtaining-context-information-for-deferred-execution-custom-actions.md) personalizada diferida escrita en script debe usar uno de los métodos o propiedades del objeto **Session** descritos en la sección Obtención de información de contexto para acciones personalizadas de ejecución aplazada para recuperar su contexto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 



