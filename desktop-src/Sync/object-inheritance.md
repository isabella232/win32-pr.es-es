---
description: Al crear un proceso con la función CreateProcess, puede especificar que el proceso herede identificadores para los objetos mutex, event, semaphore o timer mediante la estructura SECURITY \_ ATTRIBUTES.
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Herencia de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab6d2380ac0012e0f1005df2dfc4b820bee82a7974f3ca03d856c7df9fb8446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661385"
---
# <a name="object-inheritance"></a>Herencia de objetos

Al crear un proceso con la función [**CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) puede especificar que el proceso herede identificadores para los objetos mutex, event, semaphore o timer mediante la estructura [**SECURITY \_ ATTRIBUTES.**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) El identificador heredado por el proceso tiene el mismo acceso al objeto que el identificador original. El identificador heredado aparece en la tabla de identificadores del proceso creado, pero debe comunicar el valor del identificador al proceso creado. Para ello, especifique el valor como argumento de línea de comandos al llamar a **CreateProcess.** A continuación, el proceso creado usa la [**función GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) para recuperar la cadena de línea de comandos y convertir el argumento handle en un identificador utilizable. Para obtener más información, vea [Herencia](../procthread/inheritance.md).

 

 
