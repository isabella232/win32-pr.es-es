---
description: Describe los bloqueos oportunistas de nivel 1, nivel 2, Batch y Filter.
ms.assetid: 06136348-0c08-4e9c-9c96-fd3af33cbdc0
title: Tipos de bloqueos oportunistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a755a6ff766f5d19e13d4b269c1ba4bb9803e934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912309"
---
# <a name="types-of-opportunistic-locks"></a>Tipos de bloqueos oportunistas

Las operaciones de bloqueo oportunista funcionan con cuatro tipos de bloqueos oportunistas: nivel 1, nivel 2, lote y filtro. Los *bloqueos oportunistas exclusivos* son los bloqueos de nivel 1, lote y filtro. Si un subproceso tiene cualquier tipo de bloqueo exclusivo en un archivo, tampoco puede tener un bloqueo de nivel 2 en el mismo archivo.

## <a name="level-1-opportunistic-locks"></a>Bloqueos oportunistas de nivel 1

Un bloqueo oportunista de nivel 1 en un archivo permite a un cliente leer con anterioridad en el archivo y almacenar en caché datos de lectura y escritura desde el archivo localmente. Siempre que el cliente tenga acceso único a un archivo, no habrá ningún peligro en la coherencia de los datos al proporcionar un bloqueo oportunista de nivel 1.

El cliente puede solicitar un bloqueo oportunista de nivel 1 después de abrir un archivo. Si ningún otro cliente (o ningún otro subproceso en el mismo cliente) tiene abierto el archivo, el servidor puede conceder el bloqueo oportunista. Después, el cliente puede almacenar en caché los datos de lectura y escritura del archivo localmente. Si otro cliente ha abierto el archivo, el servidor rechaza el bloqueo oportunista y el cliente no realiza almacenamiento en caché local. (El servidor puede rechazar el bloqueo oportunista por otras razones, como no admitir bloqueos oportunistas).

Cuando el servidor abre un archivo que ya tiene un bloqueo oportunista de nivel 1 en él, el servidor examina el estado de uso compartido del archivo antes de interrumpir el bloqueo oportunista de nivel 1. Si el servidor interrumpe el bloqueo después de este examen, el tiempo que el cliente con el bloqueo anterior invierte en la caché de escritura es el momento en que el cliente que solicita el archivo debe esperar. Este gasto de tiempo significa que los bloqueos oportunistas de nivel 1 deben evitarse en los archivos que muchos clientes abren.

Sin embargo, dado que el servidor comprueba el estado de uso compartido antes de que interrumpa el bloqueo, en el caso en el que el servidor denegaría una solicitud abierta debido a un conflicto de uso compartido, el servidor no interrumpirá el bloqueo. Por ejemplo, si ha abierto un archivo, ha denegado el uso compartido de las operaciones de escritura y ha obtenido un bloqueo de nivel 1, el servidor deniega la solicitud de otro cliente para abrir el archivo para su escritura antes de que incluso examine el bloqueo en el archivo. En esta instancia, el bloqueo oportunista no se interrumpe.

Para ver un ejemplo de cómo funciona un bloqueo oportunista de nivel 1, consulte el ejemplo de bloqueo oportunista de nivel 1. Para obtener más información sobre cómo interrumpir los bloqueos oportunistas, vea [romper bloqueos oportunistas](breaking-opportunistic-locks.md).

## <a name="level-2-opportunistic-locks"></a>Bloqueos oportunistas de nivel 2

Un bloqueo oportunista de nivel 2 informa a un cliente de que hay varios clientes simultáneos de un archivo y que ninguno lo ha modificado todavía. Este bloqueo permite al cliente realizar operaciones de lectura y obtener atributos de archivo mediante la información local en caché o de lectura previa, pero el cliente debe enviar al servidor todas las demás solicitudes (por ejemplo, para las operaciones de escritura). La aplicación debe usar el bloqueo oportunista de nivel 2 cuando espera que otras aplicaciones escriban en el archivo de forma aleatoria o lean el archivo de forma aleatoria o secuencial.

Un bloqueo oportunista de nivel 2 es muy similar a un bloqueo oportunista de filtro. En la mayoría de los casos, la aplicación debe usar el bloqueo oportunista de nivel 2. Use solo el bloqueo de filtro si no desea que las operaciones de lectura estén abiertas para que se produzcan infracciones del modo de uso compartido en el intervalo de tiempo entre la aplicación que abre el archivo y recibe el bloqueo. Para obtener más información, vea filtrar bloqueos oportunistas y [respuesta del servidor para abrir solicitudes en archivos bloqueados](server-response-to-open-requests-on-locked-files.md).

Para obtener más información sobre cómo interrumpir los bloqueos oportunistas, vea [romper bloqueos oportunistas](breaking-opportunistic-locks.md).

## <a name="batch-opportunistic-locks"></a>Bloqueos oportunistas por lotes

Un bloqueo oportunista por lotes manipula las aperturas de archivos y los cierres. Por ejemplo, en la ejecución de un archivo por lotes, el archivo por lotes se puede abrir y cerrar una vez por cada línea del archivo. Un bloqueo oportunista por lotes abre el archivo por lotes en el servidor y lo mantiene abierto. Cuando el procesador de comandos "se abre" y "cierra" el archivo por lotes, el redirector de red intercepta los comandos de apertura y cierre. Todas las recepciones de servidor son los comandos de búsqueda y lectura. Si el cliente también está leyendo de antemano, el servidor recibe una solicitud de lectura determinada al menos una vez.

Al abrir un archivo que ya tiene un bloqueo oportunista de lotes, el servidor comprueba el estado de uso compartido del archivo después de interrumpir el bloqueo. Esta comprobación proporciona al titular del bloqueo una oportunidad para completar el vaciado de su memoria caché y cerrar el identificador de archivo. Una operación de apertura intentada durante la comprobación de uso compartido no hace que se produzca un error en la comprobación de uso compartido si el titular del bloqueo libera el bloqueo.

Para ver un ejemplo de cómo funciona un bloqueo oportunista de batch, consulte ejemplo de bloqueo oportunista de batch. Para obtener más información sobre cómo interrumpir los bloqueos oportunistas, vea [romper bloqueos oportunistas](breaking-opportunistic-locks.md).

## <a name="filter-opportunistic-locks"></a>Filtrar bloqueos oportunistas

Un bloqueo oportunista de filtro bloquea un archivo para que no se pueda abrir para el acceso de escritura o eliminación. Todos los clientes deben poder compartir el archivo. Los bloqueos de filtro permiten a las aplicaciones realizar operaciones de filtrado no intrusivo en los datos de archivo (por ejemplo, un compilador que abra código fuente o un programa de catalogación).

Un bloqueo oportunista de filtro difiere de un bloqueo oportunista de nivel 2 en que permite que se produzcan operaciones de lectura sin infracciones del modo de uso compartido en el intervalo de tiempo entre la aplicación que abre el archivo y la recepción del bloqueo. El bloqueo oportunista de filtro es el mejor bloqueo que se puede usar cuando es importante permitir que otros clientes lean el acceso. En otros casos, la aplicación debe usar un bloqueo oportunista de nivel 2. Un bloqueo oportunista de filtro difiere de un bloqueo oportunista de batch en que no permite que el redirector de red controle varias aperturas y cierres para que el redirector de la red lo lleve a cabo un bloqueo oportunista de batch.

La aplicación debe solicitar un bloqueo oportunista de filtro en un archivo en tres pasos:

1.  Use la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir un identificador para el archivo con el parámetro *DesiredAccess* establecido en cero, lo que indica que no hay acceso y el parámetro *dwShareMode* establecido en la marca **\_ \_ Read del recurso compartido de archivos** para permitir el uso compartido para la lectura. El identificador obtenido en este punto se denomina identificador de bloqueo.
2.  Solicite un bloqueo en este identificador con el código de control de [**\_ \_ \_ bloqueo oportunista del filtro de solicitud de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock) .
3.  Cuando se concede el bloqueo, use [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para volver a abrir el archivo con *DesiredAccess* establecido en la marca de **\_ lectura genérica** . Establezca *dwShareMode* en la marca de **\_ \_ lectura del recurso compartido de archivos** para que otros usuarios puedan leer el archivo mientras está abierto, la marca de **\_ \_ eliminación del recurso compartido de archivos** para permitir que otros usuarios marquen el archivo para su eliminación mientras está abierto, o ambos. El identificador obtenido en este punto se denomina controlador de lectura.

Use el controlador de lectura para leer el contenido del archivo o escribir en él.

Al abrir un archivo que ya tiene un bloqueo oportunista de filtro, el servidor interrumpe el bloqueo y, a continuación, comprueba el estado de uso compartido del archivo. Esta comprobación proporciona al cliente que mantuvo el anterior bloqueo oportunista una oportunidad de abandonar los datos almacenados en caché y confirmar la interrupción. Una operación de apertura intentada durante esta comprobación de uso compartido no hace que se produzca un error en la comprobación de uso compartido si el titular del bloqueo anterior libera el bloqueo. El sistema de archivos mantiene en abeyance la operación de apertura hasta que el propietario del bloqueo cierra tanto el controlador de lectura como el identificador de bloqueo. Una vez hecho esto, la solicitud de apertura de otro cliente puede continuar.

Para obtener más información sobre cómo interrumpir los bloqueos oportunistas, vea [romper bloqueos oportunistas](breaking-opportunistic-locks.md).

 

 
