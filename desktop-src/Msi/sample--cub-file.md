---
description: 'Este ejemplo muestra el diseño de un archivo. Cub que contiene dos CIEM. El instalador ejecuta las acciones personalizadas en la secuencia: ICE01 y ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Archivo. Cub de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001099"
---
# <a name="sample-cub-file"></a>Archivo. Cub de ejemplo

Este ejemplo muestra el diseño de un archivo. Cub que contiene dos [CIEM](internal-consistency-evaluators-ices.md). El instalador ejecuta las acciones personalizadas en la secuencia: ICE01 y ICE08.

La acción personalizada ICE01 es un [tipo de acción personalizada 1](custom-action-type-1.md). Es un punto de entrada a un archivo DLL que se almacena como una secuencia en el archivo. Cub. Esta secuencia aparece en la tabla binaria ice.dll.

La acción personalizada ICE08 es un [tipo de acción personalizada 6](custom-action-type-6.md). Es un punto de entrada a una función de VBScript que se almacena como una secuencia en el archivo. Cub. Esta secuencia aparece en la tabla binaria como ice.vbs.

[Tabla binaria](binary-table.md)



| Nombre    | Datos                               |
|---------|------------------------------------|
| ice.vbs | Datos binarios sin formato de ice.vbs |
| ice.dll | Datos binarios sin formato de ice.dll |



 

[Tabla CustomAction](customaction-table.md)



| Acción | Tipo | Source  | Destino |
|--------|------|---------|--------|
| ICE01  | 1    | ice.dll | ICE01  |
| ICE08  | 6    | ice.vbs | ICE02  |



 

\_Tabla ICESequence



| Acción | Condición | Secuencia |
|--------|-----------|----------|
| ICE01  |           | 10       |
| ICE08  |           | 20       |



 

\_Tabla especial

ICE01 y ICE08 no requieren la inclusión de tablas de procesamiento especiales. Cuando el archivo. Cub contiene tablas especiales, también deben incluirse en la \_ tabla de validación.

[\_Tabla de validación](-validation-table.md)



| Tabla         | Columna    | Nullable | MinValue | MaxValue | KeyTable | KeyColumn | Category                         | Set | Descripción |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| Binary        | Nombre      | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| Binary        | Datos      | N        |          |          |          |           | [Binario](binary.md)             |     |             |
| CustomAction  | Acción    | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| CustomAction  | Tipo      | N        |          |          |          |           | [Entero](integer.md)           |     |             |
| CustomAction  | Source    | Y        |          |          |          |           | [CustomSource](customsource.md) |     |             |
| CustomAction  | Destino    | Y        |          |          |          |           | [Formatea](formatted.md)       |     |             |
| \_ICESequence | Acción    | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| \_ICESequence | Condición | Y        |          |          |          |           | [Condition](condition.md)       |     |             |
| \_ICESequence | Secuencia  | Y        |          |          |          |           | [Entero](integer.md)           |     |             |



 

 

 



