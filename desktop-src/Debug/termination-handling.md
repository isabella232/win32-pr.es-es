---
description: Un controlador de terminación garantiza que se ejecuta un bloque de código específico cada vez que el flujo de control deja un cuerpo de código determinado. Un controlador de terminación consta de los siguientes elementos.
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: Control de terminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23e2c81465ab9d469d3d5c503c12f5bf1c7a333507d302f3e5639e0158834e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292965"
---
# <a name="termination-handling"></a>Control de terminación

Un *controlador de* terminación garantiza que se ejecuta un bloque de código específico cada vez que el flujo de control deja un cuerpo de código determinado. Un controlador de terminación consta de los siguientes elementos.

-   Un cuerpo de código guardado
-   Un bloque de código de terminación que se va a ejecutar cuando el flujo de control sale del cuerpo guardado

Los controladores de terminación se declaran en sintaxis específica del lenguaje. Mediante el compilador de optimización de Microsoft C/C++, se implementan mediante **\_ \_ try** y **\_ \_ finally**. Para obtener más información, vea [Sintaxis del controlador](handler-syntax.md).

El cuerpo de código guardado puede ser un bloque de código, un conjunto de bloques anidados o un procedimiento o función completos. Cada vez que se ejecuta el cuerpo guardado, se ejecutará el bloque de código de terminación. La única excepción a esto es cuando el subproceso finaliza durante la ejecución del cuerpo guardado (por ejemplo, si se llama a la función [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) o [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) desde el cuerpo guardado).

El bloque de terminación se ejecuta cuando el flujo de control deja el cuerpo guardado, independientemente de si el cuerpo protector finalizó de forma normal o anómala. Se considera que el cuerpo con protección ha finalizado con normalidad cuando se ejecuta la última instrucción del bloque y el control continúa secuencialmente en el bloque de finalización. La terminación anómala se produce cuando el flujo de control deja el cuerpo guardado debido a una excepción o debido a una instrucción de control como **return**, **goto,** **break** o **continue**. Se [**puede llamar a la función AbnormalTermination**](abnormaltermination.md) desde el bloque de terminación para determinar si el cuerpo guardado finalizó con normalidad.

 

 
