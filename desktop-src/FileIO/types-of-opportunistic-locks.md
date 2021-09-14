---
description: Describe los bloqueos oportunistas de nivel 1, nivel 2, lote y filtro.
ms.assetid: 06136348-0c08-4e9c-9c96-fd3af33cbdc0
title: Tipos de bloqueos oportunistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a755a6ff766f5d19e13d4b269c1ba4bb9803e934
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069811"
---
# <a name="types-of-opportunistic-locks"></a>Tipos de bloqueos oportunistas

Las operaciones de bloqueo oportunista funcionan con cuatro tipos de bloqueos oportunistas: nivel 1, nivel 2, lote y filtro. *Los bloqueos oportunistas exclusivos* son bloqueos de nivel 1, por lotes y de filtro. Si un subproceso tiene cualquier tipo de bloqueo exclusivo en un archivo, no puede tener también un bloqueo de nivel 2 en el mismo archivo.

## <a name="level-1-opportunistic-locks"></a>Bloqueos oportunistas de nivel 1

Un bloqueo oportunista de nivel 1 en un archivo permite a un cliente leer con antelación en el archivo y almacenar en caché los datos de lectura y escritura del archivo localmente. Siempre que el cliente tenga acceso único a un archivo, no hay ningún riesgo para la coherencia de los datos al proporcionar un bloqueo oportunista de nivel 1.

El cliente puede solicitar un bloqueo oportunista de nivel 1 después de abrir un archivo. Si ningún otro cliente (o ningún otro subproceso del mismo cliente) tiene abierto el archivo, el servidor puede conceder el bloqueo oportunista. A continuación, el cliente puede almacenar en caché los datos de lectura y escritura del archivo localmente. Si otro cliente ha abierto el archivo, el servidor rechaza el bloqueo oportunista y el cliente no realiza ningún almacenamiento en caché local. (El servidor también puede rechazar el bloqueo oportunista por otros motivos, como no admitir bloqueos oportunistas).

Cuando el servidor abre un archivo que ya tiene un bloqueo oportunista de nivel 1, el servidor examina el estado de uso compartido del archivo antes de que se interrumpe el bloqueo oportunista de nivel 1. Si el servidor interrumpe el bloqueo después de este examen, el tiempo que el cliente con el bloqueo anterior dedica a vaciar su caché de escritura es el tiempo que el cliente que solicita el archivo debe esperar. Este gasto de tiempo significa que se deben evitar bloqueos oportunistas de nivel 1 en los archivos que muchos clientes abren.

Sin embargo, dado que el servidor comprueba el estado de uso compartido antes de interrumpir el bloqueo, en el caso de que el servidor deniegue una solicitud abierta debido a un conflicto de uso compartido, el servidor no interrumpe el bloqueo. Por ejemplo, si ha abierto un archivo, ha denegado el uso compartido para operaciones de escritura y ha obtenido un bloqueo de nivel 1, el servidor deniega la solicitud de otro cliente de abrir el archivo para escribirlo antes incluso de examinar el bloqueo en el archivo. En este caso, el bloqueo oportunista no se ha roto.

Para obtener un ejemplo de cómo funciona un bloqueo oportunista de nivel 1, vea Ejemplo de bloqueo oportunista de nivel 1. Para obtener más información sobre la separación de bloqueos [oportunistas, vea Breaking Opportunistic Locks](breaking-opportunistic-locks.md).

## <a name="level-2-opportunistic-locks"></a>Bloqueos oportunistas de nivel 2

Un bloqueo oportunista de nivel 2 informa a un cliente de que hay varios clientes simultáneos de un archivo y que ninguno lo ha modificado todavía. Este bloqueo permite al cliente realizar operaciones de lectura y obtener atributos de archivo mediante información local almacenada en caché o de lectura previa, pero el cliente debe enviar todas las demás solicitudes (por ejemplo, para las operaciones de escritura) al servidor. La aplicación debe usar el bloqueo oportunista de nivel 2 cuando espera que otras aplicaciones escriban en el archivo aleatoriamente o lean el archivo de forma aleatoria o secuencial.

Un bloqueo oportunista de nivel 2 es muy similar a un bloqueo oportunista de filtro. En la mayoría de las situaciones, la aplicación debe usar el bloqueo oportunista de nivel 2. Use solo el bloqueo de filtro si no desea que las operaciones abiertas de lectura causen infracciones en el modo de uso compartido en el intervalo de tiempo entre la apertura del archivo de la aplicación y la recepción del bloqueo. Para obtener más información, vea Filtrar bloqueos oportunistas y Respuesta del servidor para abrir [solicitudes en archivos bloqueados.](server-response-to-open-requests-on-locked-files.md)

Para obtener más información sobre la separación de bloqueos [oportunistas, vea Breaking Opportunistic Locks](breaking-opportunistic-locks.md).

## <a name="batch-opportunistic-locks"></a>Bloqueos oportunistas de Batch

Un bloqueo oportunista por lotes manipula las aperturas y cierres de archivos. Por ejemplo, en la ejecución de un archivo por lotes, el archivo por lotes se puede abrir y cerrar una vez para cada línea del archivo. Un bloqueo oportunista por lotes abre el archivo por lotes en el servidor y lo mantiene abierto. A medida que el procesador de comandos "abre" y "cierra" el archivo por lotes, el redirector de red intercepta los comandos abrir y cerrar. Todos los servidores que recibe son los comandos de búsqueda y lectura. Si el cliente también está leyendo con antelación, el servidor recibe una solicitud de lectura determinada como máximo una vez.

Al abrir un archivo que ya tiene un bloqueo oportunista por lotes, el servidor comprueba el estado de uso compartido del archivo después de romper el bloqueo. Esta comprobación ofrece al titular del bloqueo la oportunidad de completar el vaciado de la memoria caché y cerrar el identificador de archivo. Una operación abierta intentada durante la comprobación de uso compartido no provoca un error en la comprobación de uso compartido si el titular del bloqueo libera el bloqueo.

Para obtener un ejemplo de cómo funciona un bloqueo oportunista por lotes, consulte Ejemplo de bloqueo oportunista de Batch. Para obtener más información sobre la separación de bloqueos [oportunistas, vea Breaking Opportunistic Locks](breaking-opportunistic-locks.md).

## <a name="filter-opportunistic-locks"></a>Filtrar bloqueos oportunistas

Un bloqueo oportunista de filtro bloquea un archivo para que no se pueda abrir para el acceso de escritura o eliminación. Todos los clientes deben poder compartir el archivo. Los bloqueos de filtro permiten a las aplicaciones realizar operaciones de filtrado no intrusivas en los datos de archivo (por ejemplo, un código fuente de apertura del compilador o un programa de catalogación).

Un bloqueo oportunista de filtro difiere de un bloqueo oportunista de nivel 2 en que permite que las operaciones abiertas de lectura se produzcan sin infracciones del modo de uso compartido en el intervalo de tiempo entre la apertura del archivo y la recepción del bloqueo de la aplicación. El bloqueo oportunista de filtro es el mejor bloqueo que se puede usar cuando es importante permitir el acceso de lectura a otros clientes. En otros casos, la aplicación debe usar un bloqueo oportunista de nivel 2. Un bloqueo oportunista de filtro difiere de un bloqueo oportunista por lotes, ya que no permite que el redirector de red controle varias aperturas y cierres de la forma en que lo hace un bloqueo oportunista por lotes.

La aplicación debe solicitar un bloqueo oportunista de filtro en un archivo en tres pasos:

1.  Use la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir un identificador en el archivo con el parámetro *DesiredAccess* establecido en cero, que indica que no hay acceso, y el parámetro *dwShareMode* establecido en la marca **FILE SHARE \_ \_ READ** para permitir el uso compartido de lectura. El identificador obtenido en este momento se denomina identificador de bloqueo.
2.  Solicite un bloqueo en este identificador con el código de control [**FSCTL \_ REQUEST FILTER \_ \_ OPLOCK.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)
3.  Cuando se conceda el bloqueo, use [**CreateFile para**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) volver a abrir el archivo con *DesiredAccess* establecido en la **marca DE \_ LECTURA** GENÉRICA. Establezca *dwShareMode* en la marca DE LECTURA DEL RECURSO COMPARTIDO DE ARCHIVOS para permitir que otros usuarios lean el archivo mientras lo tiene abierto, la marca **FILE SHARE \_ \_ DELETE** para permitir que otros usuarios marquen el archivo para su eliminación mientras lo tiene abierto, o ambos. **\_ \_** El identificador obtenido en este momento se denomina identificador de lectura.

Use el identificador de lectura para leer o escribir en el contenido del archivo.

Al abrir un archivo que ya tiene un bloqueo oportunista de filtro, el servidor interrumpe el bloqueo y, a continuación, comprueba el estado de uso compartido del archivo. Esta comprobación ofrece al cliente que tenía el bloqueo oportunista anterior la oportunidad de abandonar los datos almacenados en caché y confirmar la interrupción. Una operación abierta intentada durante esta comprobación de uso compartido no hace que la comprobación de uso compartido no se pueda realizar si el titular del bloqueo anterior libera el bloqueo. El sistema de archivos mantiene presionada la operación de apertura hasta que el propietario del bloqueo cierra el identificador de lectura y, a continuación, el identificador de bloqueo. Una vez hecho esto, la solicitud abierta del otro cliente puede continuar.

Para obtener más información sobre la separación de bloqueos [oportunistas, vea Breaking Opportunistic Locks](breaking-opportunistic-locks.md).

 

 
