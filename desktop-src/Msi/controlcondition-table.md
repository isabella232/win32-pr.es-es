---
description: La tabla ControlCondition permite que un autor especifique acciones especiales que se aplicarán a los controles basándose en el resultado de una instrucción condicional. Por ejemplo, al usar esta tabla, el autor podría optar por ocultar un control basado en la propiedad VersionNT.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Tabla ControlCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002371"
---
# <a name="controlcondition-table"></a>Tabla ControlCondition

La tabla ControlCondition permite que un autor especifique acciones especiales que se aplicarán a los controles basándose en el resultado de una instrucción condicional. Por ejemplo, al usar esta tabla, el autor podría optar por ocultar un control basado en la propiedad [**VersionNT**](versionnt.md) .

La tabla ControlCondition tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Diálogo\_  | [Identificador](identifier.md) | Y   | N        |
| control\_ | [Identificador](identifier.md) | Y   | N        |
| Acción    | [Texto](text.md)             | Y   | N        |
| Condición | [Condition](condition.md)   | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Diálogo\_
</dt> <dd>

Una clave externa a la primera columna de la [tabla del cuadro de diálogo](dialog-table.md). La combinación de este campo con el campo de control \_ identifica un control único.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_
</dt> <dd>

Una clave externa a la segunda columna de la [tabla de control](control-table.md). Al combinar este campo, el campo del cuadro de diálogo \_ identifica un control único.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar
</dt> <dd>

Acción que se va a realizar en el control. En la tabla siguiente se muestran las acciones posibles.



| Value   | Significado                     |
|---------|-----------------------------|
| Valor predeterminado | Establecer el control como el valor predeterminado. |
| Disable | Deshabilite el control.        |
| Habilitar  | Habilite el control.         |
| Ocultar    | Oculte el control.           |
| Mostrar    | Mostrar el control.        |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple
</dt> <dd>

Instrucción condicional que especifica en qué condiciones se debe desencadenar la acción. Esta columna no se puede dejar en blanco. Si esta instrucción no se evalúa como TRUE, la acción no tiene lugar. Si se establece en 1, siempre se aplica la acción. Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si desea ocultar y deshabilitar un control [Pushbutton](pushbutton-control.md) o un [control de casilla](checkbox-control.md) basado en una instrucción condicional en el campo condición de la tabla ControlCondition, debe usar cuatro registros para que cada control se deshabilite y oculte el control. Todavía se puede tener acceso a los controles de pulsador o casilla que solo se han ocultado mediante teclas de método abreviado.

Por ejemplo, los registros siguientes ocultan y deshabilitan controla en el cuadro de diálogo cuando se instala el producto. El control estará visible y habilitado cuando el producto no esté instalado.



| Diálogo  | Control  | Acción  | Condición                      |
|---------|----------|---------|--------------------------------|
| Cuadro de diálogo | ControlA | Ocultar    | [**Instalado**](installed.md) |
| Cuadro de diálogo | ControlA | Disable | Instalado                      |
| Cuadro de diálogo | ControlA | Mostrar    | NO instalado                  |
| Cuadro de diálogo | ControlA | Habilitar  | NO instalado                  |



 

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



