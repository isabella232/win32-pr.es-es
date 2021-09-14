---
description: Los desarrolladores Windows paquetes del instalador pueden optar por usar una acción personalizada de tipo 50 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Tipo de acción personalizada 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f3a80de730eb727c40c871070ab9e5b2470f98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158680"
---
# <a name="custom-action-type-50"></a>Tipo de acción personalizada 50

Esta acción personalizada llama a un ejecutable iniciado con una línea de comandos.

Vea también [Archivos ejecutables](executable-files.md).

## <a name="source"></a>Source

El archivo ejecutable se genera a partir de un archivo existente. El campo Source de la [tabla CustomAction contiene](customaction-table.md) una clave para la tabla [Property](property-table.md) de una propiedad que contiene la ruta de acceso completa al archivo ejecutable.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                        | Hexadecimal | Decimal |
|------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty** | 0x032       | 50      |



 

## <a name="target"></a>Destino

La columna Target de la [tabla CustomAction contiene](customaction-table.md) la cadena de línea de comandos para el ejecutable identificado en la columna Source.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de devolución. Para obtener una descripción de las opciones y los valores, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction para](customaction-table.md) especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Las acciones personalizadas que [son archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente. El instalador interpreta cualquier otro valor devuelto como error. Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la tabla CustomAction.

## <a name="remarks"></a>Observaciones

Una acción personalizada que inicia un ejecutable toma una línea de comandos, que normalmente contiene propiedades que se designan dinámicamente. Si también se trata de una acción personalizada [de](deferred-execution-custom-actions.md)ejecución aplazada, el instalador usa CreateProcessAsUser o CreateProcess para crear el proceso cuando se invoca la acción personalizada desde el script de instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 



