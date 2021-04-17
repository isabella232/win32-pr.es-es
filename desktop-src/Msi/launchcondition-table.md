---
description: La acción LaunchConditions usa la tabla LaunchCondition. Contiene una lista de condiciones que se deben satisfacer para que se inicie la instalación.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: Tabla LaunchCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686803"
---
# <a name="launchcondition-table"></a>Tabla LaunchCondition

La [acción LaunchConditions](launchconditions-action.md)usa la tabla LaunchCondition. Contiene una lista de condiciones que se deben satisfacer para que se inicie la instalación.

La tabla LaunchCondition tiene las columnas siguientes.



| Columna      | Tipo                       | Clave | Nullable |
|-------------|----------------------------|-----|----------|
| Condición   | [Condition](condition.md) | Y   | N        |
| Descripción | [Formatea](formatted.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple
</dt> <dd>

Expresión que debe evaluarse como true para que se inicie la instalación.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Texto localizable que se muestra cuando se produce un error en la condición y se debe terminar la instalación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

No se puede garantizar el orden en el que se evalúan las condiciones de inicio mediante la creación de esta tabla. Si es necesario controlar el orden en el que se evalúan las condiciones, debe hacerlo con las acciones personalizadas del tipo de acción personalizada 19 en la instalación.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



