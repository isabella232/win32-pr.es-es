---
description: Un controlador de terminación garantiza que se ejecute un bloque de código específico cada vez que el flujo de control deje un cuerpo de código determinado. Un controlador de terminación consta de los siguientes elementos.
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: Control de terminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e926a47a3c0bb4f2cb8a8df350807aee89b49bab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164562"
---
# <a name="termination-handling"></a>Control de terminación

Un *controlador de* terminación garantiza que se ejecute un bloque de código específico cada vez que el flujo de control deje un cuerpo de código determinado. Un controlador de terminación consta de los siguientes elementos.

-   Un cuerpo de código guardado
-   Bloque de código de terminación que se va a ejecutar cuando el flujo de control sale del cuerpo guardado

Los controladores de terminación se declaran en sintaxis específica del lenguaje. Mediante el compilador de optimización de Microsoft C/C++, se implementan mediante **\_ \_ try** **\_ \_ y, por último,**. Para obtener más información, vea [Sintaxis del controlador](handler-syntax.md).

El cuerpo de código guardado puede ser un bloque de código, un conjunto de bloques anidados o un procedimiento o función completos. Cada vez que se ejecuta el cuerpo guardado, se ejecutará el bloque de código de terminación. La única excepción a esto es cuando el subproceso finaliza durante la ejecución del cuerpo guardado (por ejemplo, si se llama a la función [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) o [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) desde dentro del cuerpo de protección).

El bloque de terminación se ejecuta cuando el flujo de control deja el cuerpo guardado, independientemente de si el cuerpo guardado finalizó de forma normal o anómala. Se considera que el cuerpo de protección ha finalizado con normalidad cuando se ejecuta la última instrucción del bloque y el control continúa secuencialmente en el bloque de terminación. La terminación anómala se produce cuando el flujo de control deja el cuerpo guardado debido a una excepción o debido a una instrucción de control como **return**, **goto,** **break** o **continue.** Se [**puede llamar a la función AbnormalTermination**](abnormaltermination.md) desde el bloque de terminación para determinar si el cuerpo guardado finalizó con normalidad.

 

 
