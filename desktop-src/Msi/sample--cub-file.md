---
description: 'En este ejemplo se muestra el diseño de un archivo .uu. que contiene dos TIC. El instalador ejecuta las acciones personalizadas en la secuencia: ICE01 e ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Archivo .uu. de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074309"
---
# <a name="sample-cub-file"></a>Archivo .uu. de ejemplo

En este ejemplo se muestra el diseño de un archivo .uu. que contiene dos [TIC.](internal-consistency-evaluators-ices.md) El instalador ejecuta las acciones personalizadas en la secuencia: ICE01 e ICE08.

La acción personalizada ICE01 es un [tipo de acción personalizada 1.](custom-action-type-1.md) Es un punto de entrada a un archivo DLL que se almacena como una secuencia en el archivo .uu. Esta secuencia se muestra en la tabla binaria ice.dll.

La acción personalizada ICE08 es un [tipo de acción personalizada 6.](custom-action-type-6.md) Es un punto de entrada a una función de VBScript que se almacena como una secuencia en el archivo .uu. Esta secuencia se muestra en la tabla binaria como ice.vbs.

[Tabla binaria](binary-table.md)



| Nombre    | Datos                               |
|---------|------------------------------------|
| ice.vbs | Datos binarios sin formato de ice.vbs |
| ice.dll | Datos binarios sin formato de ice.dll |



 

[CustomAction (tabla)](customaction-table.md)



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

ICE01 y ICE08 no requieren la inclusión de tablas de procesamiento especiales. Cuando el archivo .csv contiene tablas especiales, también deben incluirse en la \_ tabla de validación.

[\_Tabla de validación](-validation-table.md)



| Tabla         | Columna    | Nullable | MinValue | MaxValue | KeyTable | KeyColumn | Category                         | Set | Descripción |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| Binary        | Nombre      | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| Binary        | Datos      | N        |          |          |          |           | [Binario](binary.md)             |     |             |
| CustomAction  | Acción    | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| CustomAction  | Tipo      | N        |          |          |          |           | [Entero](integer.md)           |     |             |
| CustomAction  | Source    | Y        |          |          |          |           | [CustomSource](customsource.md) |     |             |
| CustomAction  | Destino    | Y        |          |          |          |           | [Formato](formatted.md)       |     |             |
| \_ICESequence | Acción    | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| \_ICESequence | Condición | Y        |          |          |          |           | [Condition](condition.md)       |     |             |
| \_ICESequence | Secuencia  | Y        |          |          |          |           | [Entero](integer.md)           |     |             |



 

 

 



