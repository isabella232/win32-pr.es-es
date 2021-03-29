---
description: El servidor de canalización especifica los modos de acceso de la canalización, superposición y escritura a través en el parámetro dwOpenMode de la función CreateNamedPipe. Los clientes de canalización pueden especificar estos modos abiertos para los identificadores de canalización mediante la función CreateFile.
ms.assetid: 88824566-93c7-4941-a4fc-3a7ae9a332a4
title: Modos de apertura de canalización con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f51d41ea98a47a269634b06ccdad869bd649fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002888"
---
# <a name="named-pipe-open-modes"></a>Modos de apertura de canalización con nombre

El servidor de canalización especifica los modos de acceso de la canalización, superposición y escritura a través en el parámetro *dwOpenMode* de la función [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . Los clientes de canalización pueden especificar estos modos abiertos para los identificadores de canalización mediante la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

## <a name="access-mode"></a>Modo de acceso

Establecer el modo de acceso de canalización es equivalente a especificar el acceso de lectura o escritura asociado a los identificadores del servidor de canalización. En la tabla siguiente se muestra el derecho de acceso genérico equivalente para cada modo de acceso que se puede especificar con [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).



| Modo de acceso            | Derecho de acceso genérico equivalente |
|------------------------|---------------------------------|
| \_entrada de acceso de canalización \_  | \_lectura genérica                   |
| acceso de CANALización \_ \_ saliente | \_escritura genérica                  |
| \_dúplex de acceso de canalización \_   | \_ \| escritura genérica de lectura genérica \_ |



 

Si el servidor de canalización crea una canalización con acceso de CANALización de \_ \_ entrada, la canalización es de solo lectura para el servidor de canalización y para el cliente de canalización de solo escritura. Si el servidor de canalización crea una canalización con acceso de CANALización de \_ \_ salida, la canalización es de solo escritura para el servidor de canalización y de solo lectura para el cliente de canalización. Una canalización creada con \_ \_ dúplex de acceso de canalización es de lectura y escritura para el servidor de canalización y el cliente de canalización.

Los clientes de canalización con [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para conectarse a una canalización con nombre deben especificar un derecho de acceso en el parámetro *dwDesiredAccess* que sea compatible con el modo de acceso especificado por el servidor de canalización. Por ejemplo, un cliente debe especificar \_ acceso de lectura genérico para abrir un identificador de una canalización que el servidor de canalización creado con acceso de canalización de \_ \_ salida. Los modos de acceso deben ser los mismos para todas las instancias de una canalización.

Para leer los atributos de canalización, como el modo de lectura o el modo de bloqueo, el identificador de canalización debe tener el \_ derecho de acceso leer atributos de archivo \_ ; para escribir atributos de canalización, el identificador de canalización debe tener el \_ derecho de acceso a los atributos de escritura de archivo \_ . Estos derechos de acceso se pueden combinar con el derecho de acceso genérico que sea adecuado para la canalización: \_ lectura genérica con \_ \_ atributos de escritura de archivo para una canalización de solo lectura o \_ escritura genérica con \_ \_ atributos de lectura de archivo para una canalización de solo escritura. Restringir los derechos de acceso de esta manera proporciona una mejor seguridad para la canalización.

## <a name="overlapped-mode"></a>Modo superpuesto

En el modo superpuesto, las funciones que realizan operaciones de lectura, escritura y conexión largas pueden volver inmediatamente. Esto permite que el subproceso realice otras operaciones mientras se ejecuta en segundo plano una operación que lleva mucho tiempo. Para especificar el modo superpuesto, use la marca de la marca de archivo \_ \_ superpuesta. Para obtener más información, vea [entrada y salida sincrónica y superpuesta](synchronous-and-overlapped-input-and-output.md).

La función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) permite que el cliente de canalización establezca el modo superpuesto ( \_ \_ superpuesto de marca de archivo) para sus controladores de canalización mediante el parámetro *dwFlagsAndAttributes* .

## <a name="write-through-mode"></a>Modo de Write-Through

Especifique el modo de escritura a través con escritura de marcador de archivo \_ \_ \_ a través. Este modo solo afecta a las operaciones de escritura en canalizaciones de tipo byte entre clientes de canalización y servidores de canalización en equipos diferentes. En el modo de escritura a través, las funciones que escriben en una canalización con nombre no vuelven hasta que los datos se transmiten a través de la red y al búfer de la canalización en el equipo remoto. El modo de escritura es útil para las aplicaciones que requieren sincronización para cada operación de escritura.

Si el modo de escritura no está habilitado, el sistema mejora la eficacia de las operaciones de red mediante el almacenamiento en búfer de los datos hasta que haya acumulado un número mínimo de bytes o hasta que haya transcurrido un período de tiempo máximo. El almacenamiento en búfer permite al sistema combinar varias operaciones de escritura en una única transmisión de red. Esto significa que una operación de escritura se puede completar correctamente después de que el sistema Coloque los datos en el búfer de salida, pero antes de que el sistema lo transmita a través de la red.

La función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) permite que el cliente de canalización establezca el modo de escritura a través ( \_ escritura de marca de archivo \_ \_ a través) para sus controladores de canalización mediante el parámetro *dwFlagsAndAttributes* . No se puede cambiar el modo de escritura a través de un identificador de canalización una vez creado el identificador de canalización. El modo de escritura diferida puede ser diferente para los identificadores de servidor y de cliente en la misma instancia de canalización.

Un cliente de canalización puede utilizar la función [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para controlar el número de bytes y el período de tiempo de espera antes de la transmisión para una canalización en la que se deshabilita el modo de escritura a través. En el caso de una canalización de solo lectura, el identificador de canalización debe abrirse con los derechos de acceso GENÉRICOs de \_ lectura y escritura de archivo \_ \_ .

 

 
