---
description: Los desarrolladores Windows paquetes del instalador pueden optar por usar un tipo de acción personalizada 38 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: Tipo de acción personalizada 38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361da558a6b1cf9d483d5cdb84d3a4290f9d25fb88ed844d564a26228378a14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947946"
---
# <a name="custom-action-type-38"></a>Tipo de acción personalizada 38

Esta acción personalizada se escribe en VBScript. Vea también [Scripts](scripts.md).

## <a name="source"></a>Source

El campo Source de la [tabla CustomAction](customaction-table.md) contiene el valor NULL. El código de script para la acción personalizada se almacena como una cadena de texto de script literal en el campo Destino.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.



| Constantes                                                              | Hexadecimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory** | 0x026       | 38      |



 

Windows El instalador puede usar acciones personalizadas de 64 bits en sistemas operativos de 64 bits. Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico. Para obtener información, [vea Acciones personalizadas de 64 bits.](64-bit-custom-actions.md) Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.



| Constantes                                                                                                     | Hexadecimal | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript** | 0x0001026   | 4134    |



 

## <a name="target"></a>Destino

El campo Target de la [tabla CustomAction contiene](customaction-table.md) el código de script para la acción personalizada como una cadena de texto de script literal.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de devolución. Para obtener una descripción de las opciones y los valores, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Este tipo de acción personalizada siempre devuelve correcto.

## <a name="remarks"></a>Comentarios

Una acción personalizada escrita en JScript o VBScript requiere la instalación del [**objeto Session.**](session-object.md) El instalador asocia el **objeto de sesión** al script con el nombre "Session". Dado que es posible que el objeto **Session** no exista durante una reversión de la instalación, una acción [](obtaining-context-information-for-deferred-execution-custom-actions.md) personalizada diferida escrita en script debe usar uno de los métodos o propiedades del objeto **Session** descritos en la sección Obtención de información de contexto para acciones personalizadas de ejecución aplazada para recuperar su contexto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 



