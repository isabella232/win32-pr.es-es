---
description: ICE79 valida las referencias a los componentes y las características especificados en los campos de la base de datos mediante el tipo de datos condition.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154812"
---
# <a name="ice79"></a>ICE79

ICE79 valida las referencias a los componentes y las características especificados en los campos de la base de datos mediante el tipo de datos [Condition](condition.md) .

## <a name="result"></a>Resultado

ICE79 expone dos advertencias.



| ADVERTENCIA de ICE79                                                                      | Descripción                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Falta la tabla de validación en la base de datos \_ . No se pudieron comprobar por completo los nombres de propiedad. | Falta la [ \_ tabla de validación](-validation-table.md)en la base de datos. |
| Error al recuperar valores de la columna \[ 2 \] de la tabla \[ 1 \] . Se omitirá la columna.         | Error al recuperar el valor.                                          |



 

ICE79 expone dos errores.



| Error ICE79                                                          | Descripción                               |
|----------------------------------------------------------------------|-------------------------------------------|
| Se hace referencia al componente '% ls ' en la columna '% s '. ' % s ' de la fila% s no es válido. | Se encontró una referencia de componente no válida. |
| Se hace referencia a la característica '% ls ' en la columna '% s '. ' % s ' de la fila% s no es válido.   | Se encontró una referencia de característica no válida    |



 

## <a name="example"></a>Ejemplo

ICE79 notifica los siguientes errores para el ejemplo:

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

En este ejemplo, NoSuchComponent no está presente en la [tabla de componentes](component-table.md) y NoSuchFeature no está presente en la tabla de [características](feature-table.md).

[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Acción  | Condición                                |
|---------|------------------------------------------|
| Especial | TESTACTION = 1046 y &NoSuchFeature>2  |
| Visión | TESTACTION = 146 y $NoSuchComponent>2 |



 

Para corregir estos errores, escriba registros válidos para NoSuchFeature y NoSuchComponent en las tablas de características y componentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



