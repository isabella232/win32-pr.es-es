---
description: Cuando se crea un proceso con la función CreateProcess, se puede especificar que el proceso herede los identificadores de los objetos mutex, Event, Semaphore o Timer mediante la estructura de atributos de seguridad \_ .
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Herencia de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667871"
---
# <a name="object-inheritance"></a>Herencia de objetos

Cuando se crea un proceso con la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , se puede especificar que el proceso herede los identificadores de los objetos mutex, Event, Semaphore o Timer mediante la estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . El identificador heredado por el proceso tiene el mismo acceso al objeto que el identificador original. El identificador heredado aparece en la tabla de identificadores del proceso creado, pero debe comunicar el valor de identificador al proceso creado. Puede hacerlo especificando el valor como un argumento de línea de comandos cuando llame a **CreateProcess**. A continuación, el proceso creado utiliza la función [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) para recuperar la cadena de línea de comandos y convertir el argumento de identificador en un identificador utilizable. Para obtener más información, vea [Herencia](../procthread/inheritance.md).

 

 
