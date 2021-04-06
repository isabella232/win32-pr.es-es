---
description: Los módulos de combinación solo funcionan con componentes y no con características. Sin embargo, algunas tablas de los módulos de combinación, como la tabla PublishComponent, contienen campos que hacen referencia a las características de.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Hacer referencia a características en módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001872"
---
# <a name="referencing-features-in-merge-modules"></a>Hacer referencia a características en módulos de combinación

Los módulos de combinación solo funcionan con componentes y no con características. Sin embargo, algunas tablas de los módulos de combinación, como la [tabla PublishComponent](publishcomponent-table.md), contienen campos que hacen referencia a las características de.

Un GUID NULL: {00000000-0000-0000-0000-000000000000} se debe crear en cualquier campo de una base de datos de módulo de combinación que haga referencia a una característica. Cuando el módulo de fusión mediante combinación se combina en un paquete de instalación, la herramienta de combinación reemplaza el GUID nulo con la característica especificada en el paquete de instalación, excepto en las tablas que requieren un tratamiento especial, como la [tabla ModuleSignature](modulesignature-table.md) y las tablas ModuleSequence.

Tenga en cuenta que si se usa un GUID NULL como clave principal, no se garantiza que el valor que sustituye a la herramienta de combinación sea único. Los autores de los módulos de combinación son los responsables de garantizar que no se duplique ninguna clave principal existente en la interfaz del usuario cuando la herramienta de fusión mediante combinación Reemplace los GUID nulos por las características de.

 

 



