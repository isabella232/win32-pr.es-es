---
description: La tabla de condiciones se puede usar para modificar el estado de selección de cualquier entrada en la tabla de características basada en una expresión condicional.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Tabla de condiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000953"
---
# <a name="condition-table"></a>Tabla de condiciones

La tabla de condiciones se puede usar para modificar el estado de selección de cualquier entrada en la [tabla de características](feature-table.md) basada en una expresión condicional.

La tabla de condiciones tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Característica\_ | [Identificador](identifier.md) | Y   | N        |
| Nivel     | [Entero](integer.md)       | Y   | N        |
| Condición | [Condition](condition.md)   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_
</dt> <dd>

Clave externa en la columna uno de la tabla de características.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Dosis
</dt> <dd>

Un nivel de instalación condicional para la característica en la \_ columna de característica de esta tabla. El instalador establece el nivel de instalación de esta característica en el nivel especificado en esta columna si la expresión de la columna condition se evalúa como TRUE.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple
</dt> <dd>

Si esta expresión condicional se evalúa como TRUE, la columna LEVEL de la tabla de características se establece en el nivel de instalación condicional.

La expresión de la columna condición no debe contener una referencia al estado instalado de cualquier característica o componente. Esto se debe a que las expresiones de la columna condición se evalúan antes de que el instalador evalúe los Estados instalados de características y componentes. Cualquier expresión de la tabla de condiciones que intenta comprobar el estado instalado de una característica o componente siempre se evalúa como false.

Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una característica se puede deshabilitar permanentemente si se establece la columna LEVEL en 0.

El nivel se puede establecer en función de cualquier instrucción condicional, como una prueba para la plataforma, el sistema operativo o un valor de propiedad determinado.

Las condiciones deben elegirse con cuidado para que una característica no esté habilitada en la instalación y deshabilitarse en la desinstalación. Esto hará que la característica quede huérfana y el producto no podrá desinstalarse.

Se hace referencia a esta tabla cuando se ejecuta la [acción CostFinalize](costfinalize-action.md) .

Si la propiedad [**preseleccionada**](preselected.md) se ha establecido en 1, el instalador no evalúa la tabla de condiciones. La tabla de condición solo afecta a la instalación de características cuando no se ha establecido ninguna de las siguientes propiedades:

<dl>

[**ADDLOCAL**](addlocal.md)  
[**RETIRAR**](remove.md)  
[**ADDSOURCE**](addsource.md)  
[**ADDDEFAULT**](adddefault.md)  
[**REINSTALAR**](reinstall.md)  
[**ANUNCIA**](advertise.md)  
[**COMPADDLOCAL**](compaddlocal.md)  
[**COMPADDSOURCE**](compaddsource.md)  
[**COMPADDDEFAULT**](compadddefault.md)  
[**FILEADDLOCAL**](fileaddlocal.md)  
[**FILEADDSOURCE**](fileaddsource.md)  
[**FILEADDDEFAULT**](fileadddefault.md)  
</dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



