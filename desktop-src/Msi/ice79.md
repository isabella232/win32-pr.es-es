---
description: ICE79 valida las referencias a componentes y características especificados en los campos de base de datos mediante el tipo de datos Condición.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074534"
---
# <a name="ice79"></a>ICE79

ICE79 valida las referencias a componentes y características especificados en los campos de base de datos mediante el tipo [de datos Condición.](condition.md)

## <a name="result"></a>Resultado

ICE79 publica dos advertencias.



| Advertencia de ICE79                                                                      | Descripción                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Falta la tabla \_ de validación de la base de datos. No se pudieron comprobar completamente los nombres de propiedad. | Falta la tabla [ \_ de validación de la base de datos](-validation-table.md). |
| Error al recuperar valores de la \[ columna 2 \] de la tabla \[ \] 1. Omitir columna.         | Error al recuperar el valor.                                          |



 

ICE79 publica dos errores.



| Error ice79                                                          | Descripción                               |
|----------------------------------------------------------------------|-------------------------------------------|
| Componente '%ls' al que se hace referencia en la columna '%s'.' %s' de la fila %s no es válido. | Se encontró una referencia de componente no válida. |
| Característica "%ls" a la que se hace referencia en la columna "%s"." %s' de la fila %s no es válido.   | Se encontró una referencia de característica no válida    |



 

## <a name="example"></a>Ejemplo

ICE79 notifica los siguientes errores para el ejemplo:

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

En este ejemplo, NoSuchComponent no está presente en la tabla [Component](component-table.md) y NoSuchFeature no aparece en la [tabla Feature](feature-table.md).

[InstallExecuteSequence Table](installexecutesequence-table.md) (parcial)



| Acción  | Condición                                |
|---------|------------------------------------------|
| Custom1 | TESTACTION=1046 AND &NoSuchFeature>2  |
| Custom2 | TESTACTION=146 Y $NoSuchComponent>2 |



 

Para corregir estos errores, escriba registros válidos para NoSuchFeature y NoSuchComponent en las tablas Feature y Component.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



