---
description: ICE79 valida las referencias a componentes y características especificados en los campos de base de datos mediante el tipo de datos Condición.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f11ab5bcf0cd538005a5188559b0426e27004cb5a6d043852be3e361d10e509
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821575"
---
# <a name="ice79"></a>ICE79

ICE79 valida las referencias a componentes y características especificados en los campos de base de datos mediante el [tipo de datos Condición.](condition.md)

## <a name="result"></a>Resultado

ICE79 publica dos advertencias.



| Advertencia de ICE79                                                                      | Descripción                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Falta la tabla \_ de validación de la base de datos. No se pudieron comprobar completamente los nombres de propiedad. | Falta la tabla [ \_ de validación de la base de datos](-validation-table.md). |
| Error al recuperar valores de la columna \[ 2 \] de la tabla \[ \] 1. Omitir columna.         | Error al recuperar el valor.                                          |



 

ICE79 publica dos errores.



| Error ICE79                                                          | Descripción                               |
|----------------------------------------------------------------------|-------------------------------------------|
| Componente '%ls' al que se hace referencia en la columna '%s'.' %s' de la fila %s no es válido. | Se encontró una referencia de componente no válida. |
| Característica "%ls" a la que se hace referencia en la columna "%s". %s' de la fila %s no es válido.   | Se encontró una referencia de característica no válida    |



 

## <a name="example"></a>Ejemplo

ICE79 notifica los siguientes errores para el ejemplo:

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

En este ejemplo, NoSuchComponent no está presente en la tabla [Component](component-table.md) y NoSuchFeature está ausente de la [tabla Feature](feature-table.md).

[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Acción  | Condición                                |
|---------|------------------------------------------|
| Custom1 | TESTACTION=1046 AND &NoSuchFeature>2  |
| Custom2 | TESTACTION=146 Y $NoSuchComponent>2 |



 

Para corregir estos errores, escriba registros válidos para NoSuchFeature y NoSuchComponent en las tablas Feature y Component.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



