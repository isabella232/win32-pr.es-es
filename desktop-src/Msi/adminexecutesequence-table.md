---
description: En la tabla AdminExecuteSequence se enumeran las acciones a las que llama el instalador en secuencia cuando se ejecuta la acción ADMIN de nivel superior.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: Tabla AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159177"
---
# <a name="adminexecutesequence-table"></a>Tabla AdminExecuteSequence

En la tabla AdminExecuteSequence se enumeran las acciones a las que llama el instalador en secuencia cuando se ejecuta la acción [ADMIN](admin-action.md) de nivel superior.

Las acciones admin de la secuencia de instalación, hasta la acción [InstallValidate](installvalidate-action.md) y los cuadros de diálogo de salida, se encuentran en la [tabla AdminUISequence](adminuisequence-table.md).

Las acciones admin de la acción InstallValidate hasta el final de la secuencia de instalación se encuentran en la tabla AdminExecuteSequence. Dado que la tabla AdminExecuteSequence debe ser independiente, también contiene las acciones de inicialización necesarias, como [LaunchConditions,](launchconditions-action.md) [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)y [CostFinalize.](costfinalize-action.md)

[Las acciones personalizadas](custom-actions.md) que requieren una interfaz de usuario deben usar [**MsiProcessMessage en**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) lugar de cuadros de diálogo creados mediante la [tabla Dialog](dialog-table.md).

Las columnas son idénticas a las de [la tabla InstallExecuteSequence](installexecutesequence-table.md). La tabla AdminExecuteSequence tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Acción    | [Identificador](identifier.md) | Y   | N        |
| Condición | [Condition](condition.md)   | N   | Y        |
| Secuencia  | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Nombre de la acción que se ejecutará. Se trata de una acción estándar o una acción personalizada enumerada en la [tabla CustomAction](customaction-table.md).

Clave de tabla principal.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Expresión lógica. Si la expresión se evalúa como false, se omite la acción. Si la sintaxis de la expresión no es válida, la secuencia finaliza y devuelve iesBadActionData. Para obtener información sobre la sintaxis de las instrucciones condicionales, vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Secuencia
</dt> <dd>

Un valor positivo indica la posición de secuencia de la acción. Los siguientes valores negativos indican que se llama a la acción si el instalador devuelve la marca de terminación. Cada marca de terminación (valor negativo) se puede usar sin más de una acción. Varias acciones pueden tener marcas de terminación, pero deben ser marcas diferentes. Las marcas de terminación (valores negativos) se usan normalmente con cuadros [de diálogo](dialog-boxes.md).



| Marca de terminación          | Value | Descripción                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Finalización correcta. Se usa con [los cuadros de](exit-dialog.md) diálogo Salir.               |
| msiDoActionStatusUserExit | -2    | El usuario finaliza la instalación. Se usa con [los cuadros de diálogo UserExit.](userexit-dialog.md)     |
| msiDoActionStatusFailure  | -3    | Finaliza la salida irrescindiendo. Se usa con cuadros [de diálogo FatalError.](fatalerror-dialog.md) |
| msiDoActionStatusSuspend  | -4    | La instalación está suspendida.                                                                |



 

Cero, todos los demás números negativos o un valor NULL indican que nunca se llama a la acción.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 



