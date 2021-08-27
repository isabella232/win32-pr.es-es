---
description: La tabla ControlCondition permite a un autor especificar acciones especiales que se aplicarán a los controles en función del resultado de una instrucción condicional. Por ejemplo, con esta tabla, el autor podría optar por ocultar un control basado en la propiedad VersionNT.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Tabla ControlCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637d9470af21ad1f8a15c2697ba34a6c9866c822c21c6f3a85241bac1309f76b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105262"
---
# <a name="controlcondition-table"></a>Tabla ControlCondition

La tabla ControlCondition permite a un autor especificar acciones especiales que se aplicarán a los controles en función del resultado de una instrucción condicional. Por ejemplo, con esta tabla, el autor podría optar por ocultar un control basado en la [**propiedad VersionNT.**](versionnt.md)

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

Clave externa de la primera columna de la tabla [Dialog](dialog-table.md). La combinación de este campo con el campo Control \_ identifica un control único.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_
</dt> <dd>

Clave externa de la segunda columna de la [tabla Control](control-table.md). Al combinar este campo, el \_ campo Diálogo identifica un control único.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Acción que se va a realizar en el control . Las acciones posibles se muestran en la tabla siguiente.



| Value   | Significado                     |
|---------|-----------------------------|
| Valor predeterminado | Establezca el control como predeterminado. |
| Deshabilitar | Deshabilite el control .        |
| Habilitar  | Habilite el control .         |
| Ocultar    | Oculte el control.           |
| Mostrar    | Mostrar el control.        |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Instrucción condicional que especifica en qué condiciones se debe desencadenar la acción. Es posible que esta columna no se haya dejado en blanco. Si esta instrucción no se evalúa como TRUE, la acción no tiene lugar. Si se establece en 1, la acción siempre se aplica. Para obtener información sobre la sintaxis de las instrucciones condicionales, vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si desea ocultar y deshabilitar un [control PushButton](pushbutton-control.md) o [un control CheckBox](checkbox-control.md) basado en una instrucción condicional en el campo Condición de la tabla ControlCondition, debe usar cuatro registros para que cada control se deshabilite y oculte el control. Todavía se puede acceder a los controles PushButton o CheckBox que solo se han ocultado mediante teclas de método abreviado.

Por ejemplo, los registros siguientes ocultan y deshabilitan ControlA en DialogA cuando se instala el producto. El control estará visible y habilitado cuando el producto no esté instalado.



| Diálogo  | Control  | Acción  | Condición                      |
|---------|----------|---------|--------------------------------|
| DialogA | ControlA | Ocultar    | [**Instalado**](installed.md) |
| DialogA | ControlA | Deshabilitar | Instalado                      |
| DialogA | ControlA | Mostrar    | NO instalado                  |
| DialogA | ControlA | Habilitar  | NO instalado                  |



 

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

 

 



