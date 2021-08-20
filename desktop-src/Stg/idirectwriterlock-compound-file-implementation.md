---
title: 'IDirectWriterLock: implementación de archivos compuestos'
description: La implementación de archivo compuesto de IDirectWriterLock proporciona una manera de abrir un archivo compuesto en modo directo con un único escritor y varios lectores.
ms.assetid: 4b247dae-d937-430a-bdb7-c47fa3c026b6
keywords:
- IDirectWriterLock Strctd Stg , implementación de archivos compuestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540806fd9c3907b53a50807a2ee60f5fdc0be9a3ad5ea753b52325533c5e9b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961885"
---
# <a name="idirectwriterlock---compound-file-implementation"></a>IDirectWriterLock: implementación de archivos compuestos

La implementación de archivo compuesto [**de IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) proporciona una manera de abrir un archivo compuesto en modo directo con un único escritor y varios lectores.

Los archivos compuestos se pueden abrir en modo directo mediante la marca STGM \_ DIRECT. La [**interfaz IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) establece la marca STGM \_ READWRITE STGM SHARE DENY WRITE como válida en modo directo sin requerir la sobrecarga de una copia \| de \_ \_ \_ instantánea.

Cuando se abre un archivo compuesto en modo de transacción mediante la marca STGM TRANSACTED, también puede tener varios lectores y un único escritor mediante la marca \_ STGM \_ READWRITE \| STGM \_ SHARE DENY \_ \_ WRITE. Sin embargo, en este caso, se realiza una copia de instantánea del archivo para los lectores. A menudo hay sobrecarga de una copia en cero.

## <a name="when-to-use"></a>Cuándo usar

Use la implementación proporcionada por el sistema de [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) al abrir un almacenamiento en modo directo (STGM DIRECT) con las marcas \_ \_ STGM READWRITE \| STGM \_ SHARE DENY \_ \_ WRITE.

Para obtener un puntero a [**IDirectWriterLock,**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)llame a **QueryInterface** en [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para obtener el objeto de almacenamiento raíz para el archivo compuesto.

Llame [**a IDirectWriterLock::WaitForWriteAccess para**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) obtener acceso de escritura exclusivo a un archivo compuesto. Llame [**a IDirectWriterLock::ReleaseWriteAccess para**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) liberar acceso de escritura exclusivo.

[**IDirectWriterLock::HaveWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-havewriteaccess) indica si el archivo está bloqueado actualmente.

## <a name="remarks"></a>Comentarios

La implementación de archivo compuesto de la característica de un solo sistema de escritura y varios lectores se basa en el bloqueo de intervalos. El sistema de escritura obtiene acceso exclusivo al almacenamiento para escribir una vez que todos los lectores actuales han cerrado el almacenamiento. Mientras el sistema de escritura está activo, los lectores posteriores no pueden abrir el almacenamiento. El escritor llama [**a IDirectWriterLock::WaitForWriteAccess para**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) obtener acceso de escritura exclusivo. A continuación, el escritor debe llamar [**a IDirectWriterLock::ReleaseWriteAccess para**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) liberar el almacenamiento.

La llamada a [**IDirectWriterLock::WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) es necesaria antes de escribir en este modo de lector único y de varios escritores. Los intentos de escribir en el archivo sin llamar a **IDirectWriterLock::WaitForWriteAccess** tienen como resultado primero STG \_ E \_ ACCESSDENIED. Este error se devuelve incluso si el escritor abrió el archivo inicialmente y ningún lector tiene el archivo abierto actualmente.

## <a name="marshaling-considerations"></a>Consideraciones de serialización

La serialización personalizada se usa normalmente cuando un archivo compuesto se serializa a otro proceso en el mismo equipo. Al serializar almacenamientos, no se tienen en cuenta los derechos de acceso y el puntero [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) se pasa al nuevo proceso con los mismos modos de acceso y derechos que el proceso de serialización original. Para obtener más información sobre los modos de acceso, [**vea STGM Constants**](stgm-constants.md). Durante la serialización, no se toman ni comprueban bloqueos para garantizar el acceso de escritura exclusivo. En este caso, no hay ninguna aplicación de la directiva de escritor único para los archivos compuestos abiertos en el modo de un solo escritor y de varios lectores. En su lugar, el cumplimiento se controla internamente mediante la implementación de archivos compuestos.

Dado que [**el puntero IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) se pasa a otro proceso durante la serialización, es posible que dos procesos tengan acceso simultáneo al mismo archivo compuesto. Aunque un autor de la llamada puede haber obtenido acceso de escritura exclusivo al almacenamiento mediante una llamada a [**IDirectWriterLock::WaitForWriteAccess,**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess)la versión serializada también puede tener acceso simultáneamente. Las versiones serializadas no se ven forzadas a cerrarse mientras el sistema de escritura único accede al archivo. En este caso, la implementación de archivo compuesto sincroniza las escrituras internamente.

Si un único sistema de escritura obtiene acceso exclusivo mediante una llamada a [**, IDirectWriterLock::WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess), el almacenamiento serializado también tiene acceso de escritura y no tiene que llamar a **IDirectWriterLock::WaitForWriteAccess**. Ambos procesos tienen acceso de escritura y la sincronización se controla mediante la implementación de archivos compuestos internos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)
</dt> </dl>

 

 




