---
description: El servidor de canalización especifica los modos de acceso de canalización, superposición y escritura a través en el parámetro dwOpenMode de la función CreateNamedPipe. Los clientes de canalización pueden especificar estos modos abiertos para sus identificadores de canalización mediante la función CreateFile.
ms.assetid: 88824566-93c7-4941-a4fc-3a7ae9a332a4
title: Modos de apertura de canalización con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f51d41ea98a47a269634b06ccdad869bd649fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172314"
---
# <a name="named-pipe-open-modes"></a>Modos de apertura de canalización con nombre

El servidor de canalización especifica los modos de acceso de canalización, superposición y escritura a través en el *parámetro dwOpenMode* de la [**función CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) Los clientes de canalización pueden especificar estos modos abiertos para sus identificadores de canalización mediante la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

## <a name="access-mode"></a>Modo de acceso

Establecer el modo de acceso de canalización equivale a especificar el acceso de lectura o escritura asociado a los identificadores del servidor de canalización. En la tabla siguiente se muestra el derecho de acceso genérico equivalente para cada modo de acceso que se puede especificar [**con CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).



| Modo de acceso            | Derecho de acceso genérico equivalente |
|------------------------|---------------------------------|
| ENTRADA DE \_ ACCESO DE \_ CANALIZACIÓN  | LECTURA \_ GENÉRICA                   |
| SALIDA \_ DE ACCESO DE \_ CANALIZACIÓN | ESCRITURA \_ GENÉRICA                  |
| DÚPLEX \_ DE ACCESO DE \_ CANALIZACIÓN   | ESCRITURA \_ GENÉRICA DE LECTURA \| \_ GENÉRICA |



 

Si el servidor de canalización crea una canalización con PIPE ACCESS INBOUND, la canalización es de solo lectura para el servidor de canalización y de solo escritura \_ para el cliente de \_ canalización. Si el servidor de canalización crea una canalización con PIPE ACCESS OUTBOUND, la canalización es de solo escritura para el servidor de canalización y de solo lectura \_ para el cliente de \_ canalización. Una canalización creada con PIPE ACCESS DUPLEX es de lectura \_ y escritura para el servidor de canalización y el cliente de \_ canalización.

Los clientes de canalización que usan [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para conectarse a una canalización con nombre deben especificar un derecho de acceso en el parámetro *dwDesiredAccess* que sea compatible con el modo de acceso especificado por el servidor de canalización. Por ejemplo, un cliente debe especificar el acceso DE LECTURA GENÉRICO para abrir un identificador para una canalización que el servidor de canalización \_ creó con PIPE \_ ACCESS \_ OUTBOUND. Los modos de acceso deben ser los mismos para todas las instancias de una canalización.

Para leer atributos de canalización como el modo de lectura o el modo de bloqueo, el identificador de canalización debe tener el derecho de acceso FILE READ ATTRIBUTES; para escribir atributos de canalización, el identificador de canalización debe tener el derecho de acceso \_ \_ FILE WRITE \_ \_ ATTRIBUTES. Estos derechos de acceso se pueden combinar con el derecho de acceso genérico adecuado para la canalización: LECTURA GENÉRICA con ATRIBUTOS DE ESCRITURA DE ARCHIVO para una canalización de solo lectura o ESCRITURA GENÉRICA con ATRIBUTOS DE LECTURA DE ARCHIVO para una canalización de \_ \_ solo \_ \_ \_ \_ escritura. Restringir los derechos de acceso de esta manera proporciona una mayor seguridad para la canalización.

## <a name="overlapped-mode"></a>Modo superpuesto

En el modo superpuesto, las funciones que realizan operaciones de lectura, escritura y conexión largas pueden devolver inmediatamente. Esto permite que el subproceso realice otras operaciones mientras se ejecuta una operación que consume mucho tiempo en segundo plano. Para especificar el modo superpuesto, use la marca FILE \_ FLAG \_ OVERLAPPED. Para obtener más información, vea Entrada y salida [sincrónicas y superpuestas.](synchronous-and-overlapped-input-and-output.md)

La [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) permite al cliente de canalización establecer el modo superpuesto (FILE FLAG OVERLAPPED) para sus identificadores de canalización mediante el \_ parámetro \_ *dwFlagsAndAttributes.*

## <a name="write-through-mode"></a>Write-Through modo de configuración

Especifique el modo de escritura a través con FILE \_ FLAG \_ WRITE \_ THROUGH. Este modo solo afecta a las operaciones de escritura en canalizaciones de tipo byte entre clientes de canalización y servidores de canalización en equipos diferentes. En el modo de escritura a través, las funciones que escriben en una canalización con nombre no se devuelven hasta que los datos se transmiten a través de la red y al búfer de la canalización en el equipo remoto. El modo de escritura a través es útil para las aplicaciones que requieren sincronización para cada operación de escritura.

Si el modo de escritura a través no está habilitado, el sistema mejora la eficacia de las operaciones de red almacenando en búfer los datos hasta que se haya acumulado un número mínimo de bytes o hasta que haya transcurrido un período de tiempo máximo. El almacenamiento en búfer permite al sistema combinar varias operaciones de escritura en una única transmisión de red. Esto significa que una operación de escritura se puede completar correctamente después de que el sistema coloca los datos en el búfer de salida, pero antes de que el sistema los transmita a través de la red.

La [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) permite al cliente de canalización establecer el modo de escritura a través (FILE FLAG WRITE THROUGH) para sus identificadores de canalización mediante el \_ parámetro \_ \_ *dwFlagsAndAttributes.* El modo de escritura a través de un identificador de canalización no se puede cambiar una vez creado el identificador de canalización. El modo de escritura a través puede ser diferente para los identificadores de servidor y cliente en la misma instancia de canalización.

Un cliente de canalización puede usar la función [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para controlar el número de bytes y el período de tiempo de espera antes de la transmisión de una canalización en la que el modo de escritura a través está deshabilitado. Para una canalización de solo lectura, el identificador de canalización debe abrirse con los derechos de acceso GENERIC \_ READ y FILE WRITE \_ \_ ATTRIBUTES.

 

 
