---
description: La acción LaunchConditions usa la tabla LaunchConditions. Contiene una lista de las condiciones que se deben cumplir para que se inicie la instalación.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: Tabla LaunchCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071978"
---
# <a name="launchcondition-table"></a>Tabla LaunchCondition

La acción LaunchConditions usa la [tabla LaunchConditions](launchconditions-action.md). Contiene una lista de las condiciones que se deben cumplir para que se inicie la instalación.

La tabla LaunchCondition tiene las columnas siguientes.



| Columna      | Tipo                       | Clave | Nullable |
|-------------|----------------------------|-----|----------|
| Condición   | [Condition](condition.md) | Y   | N        |
| Descripción | [Formato](formatted.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Expresión que debe evaluarse como True para que se inicie la instalación.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Texto localizable que se muestra cuando se produce un error en la condición y se debe finalizar la instalación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

No se puede garantizar el orden en el que se evalúan las condiciones de inicio mediante la creación de esta tabla. Si es necesario controlar el orden en el que se evalúan las condiciones, debe hacerlo mediante acciones personalizadas de tipo de acción personalizada 19 en la instalación.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



