---
description: Los desarrolladores de Windows installer pueden optar por usar una acción personalizada de tipo 53 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Tipo de acción personalizada 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b78c2dbc8aa233175eeacfa8d16521968dfceeb6b97504e639946c6284b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947896"
---
# <a name="custom-action-type-53"></a>Tipo de acción personalizada 53

Esta acción personalizada se escribe en JScript, como ECMA 262. Windows El instalador no admite JScript 1.0. Para obtener más información, vea [Scripts](scripts.md).

## <a name="source"></a>Source

El campo Source de la [tabla CustomAction](customaction-table.md) contiene un nombre de propiedad o una clave para la tabla [Property](property-table.md) de una propiedad que contiene el texto del script.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.



| Constantes                                                            | Hexadecimal | Decimal |
|----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty** | 0x035       | 53      |



 

Windows El instalador puede usar acciones personalizadas de 64 bits en sistemas operativos de 64 bits. Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico. Para obtener información, [vea Acciones personalizadas de 64 bits.](64-bit-custom-actions.md) Incluya el siguiente valor en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.



| Constantes                                                                                                   | Hexadecimal | Decimal |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript** | 0x0001035   | 4149    |



 

## <a name="target"></a>Destino

El campo Target de la [tabla CustomAction contiene](customaction-table.md) una función de script opcional. El procesamiento envía primero el script para analizarlo y, a continuación, llama a la función de script opcional.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de devolución. Para obtener una descripción de las opciones y los valores, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction para](customaction-table.md) especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Las funciones opcionales escritas en script deben devolver uno de los valores descritos en Valores devueltos [de JScript y Acciones personalizadas de VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).

## <a name="remarks"></a>Comentarios

Una acción personalizada escrita en JScript requiere el objeto [**Session de**](session-object.md) instalación. Dado que es posible que el objeto **Session** no exista durante una reversión de la instalación, una acción personalizada diferida escrita en script usa uno de los métodos descritos en Obtención de información de contexto para acciones personalizadas de ejecución [aplazada.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 



