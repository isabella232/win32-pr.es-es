---
title: 'IDirectWriterLock: implementación de archivos compuestos'
description: La implementación de archivos compuestos de IDirectWriterLock proporciona una manera de abrir un archivo compuesto en modo directo con un solo escritor y varios lectores.
ms.assetid: 4b247dae-d937-430a-bdb7-c47fa3c026b6
keywords:
- IDirectWriterLock Strctd STG, implementación de archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 861935a4c373ce03408c0e633e581e56d39623da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773987"
---
# <a name="idirectwriterlock---compound-file-implementation"></a>IDirectWriterLock: implementación de archivos compuestos

La implementación de archivos compuestos de [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) proporciona una manera de abrir un archivo compuesto en modo directo con un solo escritor y varios lectores.

Los archivos compuestos se pueden abrir en modo directo mediante la \_ marca de STGM Direct. La interfaz [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) establece el \_ marcador STGM ReadWrite \| STGM \_ share \_ Deny \_ Write como válido en modo directo sin requerir la sobrecarga de una copia de la instantánea.

Cuando se abre un archivo compuesto en el modo de transacción mediante el uso de la \_ marca STGM transacción, también puede tener varios lectores y un único escritor mediante \_ la \| marca de \_ denegación de lectura del recurso compartido STGM ReadWrite STGM \_ \_ . Sin embargo, en este caso, se realiza una copia de la instantánea del archivo para los lectores. A menudo hay sobrecarga de una copia temporal.

## <a name="when-to-use"></a>Cuándo usar

Use la implementación proporcionada por el sistema de [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) cuando abra un almacenamiento en modo directo (STGM \_ Direct) con las \_ marcas de \| \_ denegación de escritura del recurso compartido STGM ReadWrite STGM \_ \_ .

Para obtener un puntero a [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock), llame a **QueryInterface** en [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para obtener el objeto de almacenamiento raíz para el archivo compuesto.

Llame a [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) para obtener acceso exclusivo de escritura a un archivo compuesto. Llame a [**IDirectWriterLock:: ReleaseWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) para liberar el acceso de escritura exclusivo.

[**IDirectWriterLock:: HaveWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-havewriteaccess) indica si el archivo está bloqueado actualmente.

## <a name="remarks"></a>Observaciones

La implementación de archivos compuestos de la característica de un solo escritor y varios lectores se basa en el bloqueo de intervalo. El escritor obtiene acceso exclusivo al almacenamiento que se va a escribir después de que todos los lectores actuales hayan cerrado el almacenamiento. Mientras el escritor está activo, los lectores posteriores no pueden abrir el almacenamiento. El escritor llama a [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) para obtener acceso de escritura exclusivo. Después, el escritor debe llamar a [**IDirectWriterLock:: ReleaseWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) para liberar el almacenamiento.

La llamada a [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) es necesaria antes de escribir en este modo de lector único y de varios escritores. Los intentos de escribir en el archivo sin llamar a **IDirectWriterLock:: WaitForWriteAccess** primero generan STG \_ E \_ ACCESSDENIED. Este error se devuelve incluso si el escritor abrió el archivo inicialmente y ningún lector tiene abierto el archivo.

## <a name="marshaling-considerations"></a>Consideraciones sobre el cálculo de referencias

Normalmente, se utiliza el cálculo de referencias personalizado cuando se calculan las referencias de un archivo compuesto a otro proceso en el mismo equipo. Al calcular las referencias de los almacenamientos, no se tienen en cuenta los derechos de acceso y el puntero [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) se pasa al nuevo proceso con los mismos modos de acceso y derechos que el proceso de cálculo de referencias original. Para obtener más información sobre los modos de acceso, vea [**constantes STGM**](stgm-constants.md). Durante el cálculo de referencias, no se realiza ningún bloqueo ni se comprueba para garantizar el acceso exclusivo de escritura. En este caso, no hay ninguna aplicación de la Directiva de un solo escritor para los archivos compuestos abiertos en el modo de varios lectores. En su lugar, la implementación de archivo compuesto controla internamente la aplicación.

Dado que el puntero [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) se pasa a otro proceso durante el cálculo de referencias, es posible que dos procesos tengan acceso simultáneo al mismo archivo compuesto. Aunque un llamador puede haber obtenido acceso exclusivo de escritura al almacenamiento mediante una llamada a [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess), la versión de serialización también puede tener acceso a la vez. Las versiones serializadas no se pueden cerrar mientras el escritor único accede al archivo. En este caso, la implementación de archivo compuesto sincroniza las escrituras internamente.

Si un solo escritor obtiene acceso exclusivo llamando a, [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess), el almacenamiento de cálculo de referencias también tiene acceso de escritura y no tiene que llamar a **IDirectWriterLock:: WaitForWriteAccess**. Ambos procesos tienen acceso de escritura y la sincronización se controla mediante la implementación interna de archivos compuestos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)
</dt> </dl>

 

 




