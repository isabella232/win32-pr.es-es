---
description: En la tabla AdminUISequence se enumeran las acciones a las que llama el instalador en secuencia cuando se ejecuta la acción admin de nivel superior y el nivel de interfaz de usuario interno se establece en interfaz de usuario completa o interfaz de usuario reducida.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: Tabla AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12feb7080d6d97ee86456bee694cdad57eee9873c9c7f64aecf0f4bd05817cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381703"
---
# <a name="adminuisequence-table"></a>Tabla AdminUISequence

En la tabla AdminUISequence se enumeran las acciones a las que llama el instalador en secuencia cuando se ejecuta la acción [admin](admin-action.md) de nivel superior y el nivel de interfaz de usuario interno se establece en interfaz de usuario completa o interfaz de usuario reducida. El instalador omite las acciones de esta tabla si el nivel de interfaz de usuario está establecido en interfaz de usuario básica o sin interfaz de usuario. Vea [Acerca de la Interfaz de usuario](about-the-user-interface.md).

Las acciones admin de la secuencia de instalación hasta la acción [InstallValidate](installvalidate-action.md)y los cuadros de diálogo de salida se encuentran en la tabla AdminUISequence. Todas las acciones desde InstallValidate hasta el final de la secuencia de instalación se encuentran en la [tabla AdminExecuteSequence](adminexecutesequence-table.md). Dado que la tabla AdminExecuteSequence debe ser independiente, también contiene las acciones de inicialización necesarias, como [LaunchConditions,](launchconditions-action.md) [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)y [CostFinalize.](costfinalize-action.md) También tiene la [acción ExecuteAction](executeaction-action.md).

Las columnas son idénticas a las de [la tabla InstallUISequence](installuisequence-table.md). La tabla AdminUISequence tiene las siguientes columnas.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Acción    | [Identificador](identifier.md) | Y   | N        |
| Condición | [Condition](condition.md)   | N   | Y        |
| Secuencia  | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Nombre de la acción que se ejecutará. Se trata de una acción estándar, un asistente para la interfaz de usuario o una acción personalizada enumerada en la [tabla CustomAction](customaction-table.md).

Clave de tabla principal.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Expresión lógica. Si la expresión se evalúa como false, se omite la acción. Si la sintaxis de la expresión no es válida, la secuencia finaliza y devuelve iesBadActionData. Para obtener información sobre la sintaxis de las instrucciones condicionales, vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Secuencia
</dt> <dd>

Un valor positivo indica la posición de secuencia de la acción. Los siguientes valores negativos indican que se llama a la acción si el instalador devuelve la marca de terminación. Cada marca de terminación (valor negativo) se puede usar sin más de una acción. Varias acciones pueden tener marcas de terminación, pero deben ser marcas diferentes. Las marcas de terminación (valores negativos) se usan normalmente con cuadros [de diálogo](dialog-boxes.md).



| Marca de terminación          | Valor | Descripción                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Finalización correcta. Se usa con [los cuadros de](exit-dialog.md) diálogo Salir.               |
| msiDoActionStatusUserExit | -2    | El usuario finaliza la instalación. Se usa con [los cuadros de diálogo UserExit.](userexit-dialog.md)     |
| msiDoActionStatusFailure  | -3    | Finaliza la salida irrescindiendo. Se usa con cuadros [de diálogo FatalError.](fatalerror-dialog.md) |
| msiDoActionStatusSuspend  | -4    | La instalación se suspende.                                                                |



 

Cero, todos los demás números negativos o un valor NULL indican que nunca se llama a la acción.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE75](ice75.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICE96](ice96.md)  
[ICEM04](icem04.md)  
</dl>

 

 



