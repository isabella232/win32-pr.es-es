---
description: Un proceso secundario puede heredar los identificadores de su proceso primario. Un identificador heredado solo es válido en el contexto del proceso secundario. Para permitir que un proceso secundario herede los identificadores abiertos de su proceso primario, siga estos pasos.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Controlar la herencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668448"
---
# <a name="handle-inheritance"></a>Controlar la herencia

Un proceso secundario puede heredar los identificadores de su proceso primario. Un identificador heredado solo es válido en el contexto del proceso secundario. Para permitir que un proceso secundario herede los identificadores abiertos de su proceso primario, siga estos pasos.

1.  Cree el identificador con el miembro **bInheritHandle** de la estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) establecido en **true**.
2.  Cree el proceso secundario con la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , con el parámetro *BInheritHandles* establecido en **true**.

La función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) duplica un identificador que se va a usar en el proceso actual o en otro proceso. Si una aplicación duplica uno de sus identificadores para otro proceso, el identificador duplicado solo es válido en el contexto del otro proceso.

Un identificador duplicado o heredado es un valor único, pero hace referencia al mismo objeto que el identificador original. Los procesos pueden heredar o duplicar los identificadores de los siguientes tipos de objetos:

-   Token de acceso
-   Dispositivo de comunicaciones
-   Entrada de la consola
-   Búfer de pantalla de la consola
-   Escritorio
-   Directorio
-   Evento
-   Archivo
-   Asignación de archivos
-   Trabajo
-   Datagrama
-   Mutex
-   Pipe
-   Proceso
-   Clave del Registro
-   Semaphore
-   Toma de corriente
-   Thread
-   Temporizador
-   Estación de ventana

Todos los demás objetos son privados para el proceso que los creó. los identificadores de objeto no se pueden duplicar ni heredar.

Para obtener más información, vea [Herencia](/windows/desktop/ProcThread/inheritance).

 

 
