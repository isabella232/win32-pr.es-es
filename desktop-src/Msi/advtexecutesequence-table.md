---
description: En la tabla AdvtExecuteSequence se enumeran las acciones que el instalador llama cuando se ejecuta la acción de anuncio de nivel superior.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Tabla AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909122"
---
# <a name="advtexecutesequence-table"></a>Tabla AdvtExecuteSequence

En la tabla AdvtExecuteSequence se enumeran las acciones que el instalador llama cuando se ejecuta la [acción de anuncio](advertise-action.md) de nivel superior.

Solo se pueden usar las siguientes acciones en la tabla AdvtExecuteSequence. No se pueden usar acciones personalizadas en esta tabla.

[CostFinalize](costfinalize-action.md)

[CostInitialize](costinitialize-action.md)

[CreateShortcuts](createshortcuts-action.md)

[InstallFinalize](installfinalize-action.md)

[InstallInitialize](installinitialize-action.md)

[InstallValidate](installvalidate-action.md)

[MsiPublishAssemblies](msipublishassemblies-action.md)

[PublishComponents](publishcomponents-action.md)

[PublishFeatures](publishfeatures-action.md)

[PublishProduct](publishproduct-action.md)

[RegisterClassInfo](registerclassinfo-action.md)

[RegisterExtensionInfo](registerextensioninfo-action.md)

[RegisterMIMEInfo](registermimeinfo-action.md)

[RegisterProgIdInfo](registerprogidinfo-action.md)

Las columnas son idénticas a las de la [tabla InstallExecuteSequence](installexecutesequence-table.md). La tabla AdvtExecuteSequence tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Acción    | [Identificador](identifier.md) | Y   | N        |
| Condición | [Condition](condition.md)   | N   | Y        |
| Secuencia  | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar
</dt> <dd>

Nombre de la [acción estándar](standard-actions.md) que va a ejecutar el instalador. Esta es la clave principal de la tabla.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple
</dt> <dd>

Expresión lógica. Si la expresión se evalúa como false, se omite la acción. Si la sintaxis de la expresión no es válida, la secuencia finaliza y devuelve iesBadActionData. Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ
</dt> <dd>

Un valor positivo indica la posición de la secuencia de la acción. Los siguientes valores negativos indican que se llama a la acción si el instalador devuelve la marca de finalización. Cada marca de finalización (valor negativo) se puede usar sin más de una acción. Varias acciones pueden tener marcas de finalización, pero deben ser marcas diferentes. Las marcas de finalización (valores negativos) suelen usarse con [cuadros de diálogo](dialog-boxes.md).



| Marca de terminación          | Value | Descripción                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Finalización correcta. Se usa con los cuadros de diálogo de [salida](exit-dialog.md) .               |
| msiDoActionStatusUserExit | -2    | El usuario finaliza la instalación. Se usa con los cuadros de diálogo de [UserExit](userexit-dialog.md) .     |
| msiDoActionStatusFailure  | -3    | Se termina la salida grave. Se usa con un cuadro de diálogo de [FatalError](fatalerror-dialog.md) . |
| msiDoActionStatusSuspend  | -4    | La instalación está suspendida.                                                                |



 

Cero, todos los demás números negativos o un valor null indican que nunca se llama a la acción.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE72](ice72.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 



