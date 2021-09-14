---
description: Los módulos de combinación solo funcionan con componentes y no con características. Sin embargo, algunas tablas de los módulos de combinación, como la tabla PublishComponent, contienen campos que hacen referencia a características.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Hacer referencia a características en módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069702"
---
# <a name="referencing-features-in-merge-modules"></a>Hacer referencia a características en módulos de combinación

Los módulos de combinación solo funcionan con componentes y no con características. Sin embargo, algunas tablas de los módulos de combinación, como la [tabla PublishComponent](publishcomponent-table.md), contienen campos que hacen referencia a características.

Guid null: debe crearse en cualquier campo de una base de datos de módulo {00000000-0000-0000-0000-000000000000} de mezcla que haga referencia a una característica. Cuando el módulo de mezcla se combina en un paquete de instalación, la herramienta de combinación reemplaza el GUID nulo por la característica especificada en el paquete de instalación, excepto para las tablas que requieren un control especial, como la tabla [ModuleSignature](modulesignature-table.md) y las tablas ModuleSequence.

Tenga en cuenta que si se usa un GUID nulo como clave principal, no se garantiza que el valor sustituido por la herramienta de combinación sea único. Los autores de módulos de combinación son responsables de garantizar que no se duplique ninguna clave principal existente en la interfaz del usuario cuando la herramienta de combinación reemplace guid nulos por características.

 

 



