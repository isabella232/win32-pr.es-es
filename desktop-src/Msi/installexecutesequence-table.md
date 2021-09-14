---
description: En la tabla InstallExecuteSequence se enumeran las acciones que se ejecutan cuando se ejecuta la acción INSTALL de nivel superior.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: InstallExecuteSequence Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072076"
---
# <a name="installexecutesequence-table"></a>InstallExecuteSequence Table

En la tabla InstallExecuteSequence se enumeran las acciones que se ejecutan cuando se ejecuta la acción [INSTALL](install-action.md) de nivel superior.

Las acciones de la secuencia de instalación hasta la acción [InstallValidate](installvalidate-action.md)y los cuadros de diálogo de salida se encuentran en la [tabla InstallUISequence](installuisequence-table.md). Todas las acciones desde InstallValidate hasta el final de la secuencia de instalación se encuentran en la tabla InstallExecuteSequence. Dado que la tabla InstallExecuteSequence debe ser independiente, tiene las acciones de inicialización necesarias, como las acciones [LaunchConditions](launchconditions-action.md), [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)y [CostFinalize.](costfinalize-action.md)

[Las acciones personalizadas](custom-actions.md) que requieren una interfaz de usuario deben usar [**MsiProcessMessage en**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) lugar de cuadros de diálogo creados mediante la [tabla Dialog](dialog-table.md).

La tabla InstallExecuteSequence tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Acción    | [Identificador](identifier.md) | Y   | N        |
| Condición | [Condition](condition.md)   | N   | Y        |
| Secuencia  | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Nombre de la acción que se ejecutará. Se trata de una acción integrada o una acción personalizada.

Clave de tabla principal.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Este campo contiene una expresión condicional. Si la expresión se evalúa como False, se omite la acción. Si la sintaxis de expresión no es válida, la secuencia finaliza y devuelve iesBadActionData. Para obtener información sobre la sintaxis de las instrucciones condicionales, vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Secuencia
</dt> <dd>

Número que determina la posición de secuencia en la que se va a ejecutar esta acción.

Un valor positivo representa la posición de la secuencia. Un valor NULL indica que la acción no se ejecuta. Los siguientes valores negativos indican que esta acción se va a ejecutar si el instalador devuelve la marca de terminación asociada. Cada marca de terminación (valor negativo) se puede usar sin más de una acción. Varias acciones pueden tener marcas de terminación, pero deben ser marcas diferentes. Las marcas de terminación (valores negativos) se usan normalmente con cuadros [de diálogo](dialog-boxes.md).



| Marca de terminación          | Value | Descripción                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Finalización correcta. Se usa con [los cuadros de](exit-dialog.md) diálogo Salir.               |
| msiDoActionStatusUserExit | -2    | El usuario finaliza la instalación. Se usa con [los cuadros de diálogo UserExit.](userexit-dialog.md)     |
| msiDoActionStatusFailure  | -3    | Finaliza la salida irrescindiendo. Se usa con cuadros [de diálogo FatalError.](fatalerror-dialog.md) |
| msiDoActionStatusSuspend  | -4    | La instalación está suspendida.                                                                |



 

Cero, todos los demás números negativos o un valor NULL indican que la acción nunca se ejecuta.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El texto localizado para la presentación o el registro del progreso se especifica en la [tabla ActionText](actiontext-table.md).

Para obtener un ejemplo de una tabla de secuencia, vea [Usar una tabla de secuencia.](using-a-sequence-table.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
</dl>

 

 



