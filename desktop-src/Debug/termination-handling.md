---
description: Un controlador de finalización garantiza que se ejecute un bloque de código específico siempre que el flujo de control deje un determinado cuerpo de código protegido. Un controlador de terminación consta de los siguientes elementos.
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: Control de terminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e926a47a3c0bb4f2cb8a8df350807aee89b49bab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907238"
---
# <a name="termination-handling"></a>Control de terminación

Un *controlador de finalización* garantiza que se ejecute un bloque de código específico siempre que el flujo de control deje un determinado cuerpo de código protegido. Un controlador de terminación consta de los siguientes elementos.

-   Un cuerpo protegido del código
-   Un bloque de código de terminación que se va a ejecutar cuando el flujo de control abandone el cuerpo protegido

Los controladores de terminación se declaran en la sintaxis específica del lenguaje. Mediante el compilador de optimización de C/C++ de Microsoft, se implementan mediante **\_ \_ try** y **\_ \_ Finally**. Para obtener más información, vea [Sintaxis de controlador](handler-syntax.md).

El cuerpo protegido del código puede ser un bloque de código, un conjunto de bloques anidados o un procedimiento o una función completos. Siempre que se ejecute el cuerpo protegido, se ejecutará el bloque de código de terminación. La única excepción a esto es cuando el subproceso finaliza durante la ejecución del cuerpo protegido (por ejemplo, si se llama a la función [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) o [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) desde dentro del cuerpo protegido).

El bloque de finalización se ejecuta cuando el flujo de control sale del cuerpo protegido, independientemente de si el cuerpo protegido terminó con normalidad o de forma anómala. Se considera que el cuerpo protegido ha terminado con normalidad cuando se ejecuta la última instrucción del bloque y el control continúa secuencialmente en el bloque de finalización. La terminación anómala se produce cuando el flujo de control sale del cuerpo protegido debido a una excepción o debido a una instrucción de control como **Return**, **goto**, **break** o **continue**. Se puede llamar a la función [**AbnormalTermination**](abnormaltermination.md) desde el bloque de terminación para determinar si el cuerpo protegido terminó normalmente.

 

 
