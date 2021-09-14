---
title: Bloqueos de documentos
description: Bloqueos de documentos
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- Text Services Framework (TSF), bloqueos de documentos
- TSF (Text Services Framework), bloqueos de documentos
- Aplicaciones habilitadas para TSF, bloqueos de documentos
- bloqueos de documentos
- Text Services Framework (TSF),Posición de caracteres de aplicación (ACP)
- TSF (Text Services Framework),Posición de caracteres de aplicación (ACP)
- Aplicaciones habilitadas para TSF, posición de caracteres de aplicación (ACP)
- Posición de caracteres de aplicación (ACP)
- ACP (posición del carácter de aplicación)
- Text Services Framework (TSF),anchors
- TSF (Text Services Framework),anchors
- Aplicaciones habilitadas para TSF, delimitadores
- delimitadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243680"
---
# <a name="document-locks"></a>Bloqueos de documentos

## <a name="the-document-lock-protocol"></a>El protocolo de bloqueo de documentos

Para solicitar un bloqueo de documento para aplicaciones basadas en ACP, el administrador de TSF llama a [ITextStoreACP::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock). Para las aplicaciones basadas en delimitadores, el administrador de TSF llama [a ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock). La aplicación concede el bloqueo de documento llamando a [ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (aplicaciones basadas en ACP) o [ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (aplicaciones basadas en delimitadores) dentro de **RequestLock**. El bloqueo solo es válido durante la **llamada a OnLockGranted.** Cuando **OnLockGranted** vuelve, el documento se considera desbloqueado.

## <a name="types-of-document-locks"></a>Tipos de bloqueos de documentos

Hay dos tipos de bloqueos de documento: de solo lectura y de lectura y escritura. Un bloqueo de solo lectura permite al administrador leer el texto, pero no puede modificar ni insertar texto. Un bloqueo de lectura y escritura permite al administrador leer, modificar e insertar texto. Se solicita un bloqueo de solo lectura especificando TS \_ LF \_ READ en *dwFlags*. Se solicita un bloqueo de lectura/escritura especificando TS \_ LF \_ READWRITE en *dwFlags*.

## <a name="asynchronous-and-synchronous-requests"></a>Solicitudes asincrónicas y sincrónicas

Una solicitud de bloqueo puede ser sincrónica o asincrónica. El administrador solicita un bloqueo sincrónico mediante la marca TS \_ LF \_ SYNC en *dwFlags*. Si esta marca no está presente, la solicitud es asincrónica.

## <a name="granting-the-lock"></a>Concesión del bloqueo

Cuando **se llama a RequestLock,** la aplicación debe determinar si el documento está bloqueado actualmente. Si el documento no está bloqueado y no existe ningún otro motivo para denegar el bloqueo, la aplicación debe establecer *phrSession* en S OK y \_ devolver S \_ OK.

Si el documento está bloqueado y la solicitud de bloqueo es sincrónica, la aplicación debe establecer *phrSession* en TS E SYNCHRONOUS y \_ devolver S \_ \_ OK. Esto indica que no se puede conceder una solicitud sincrónica.

Si el documento está bloqueado y la solicitud de bloqueo es asincrónica, la aplicación debe poner en cola la solicitud, establecer *phrSession* en TS S ASYNC y \_ devolver S \_ \_ OK. Cuando el documento esté disponible, la aplicación debe quitar la solicitud de la cola y llamar a **OnLockGranted.** Esta cola de solicitudes de bloqueo es opcional; hay un escenario que una aplicación debe admitir. Si el documento tiene un bloqueo de solo lectura, la nueva solicitud de bloqueo es de lectura y escritura y la solicitud es asincrónica, la aplicación ha llamado a **OnLockGranted** , lo que ha provocado una llamada reentrante a **RequestLock.** La aplicación debe establecer *phrSession* en TS \_ S \_ ASYNC y devolver S \_ OK. Una vez que se devuelve la llamada a **OnLockGranted,** la aplicación debe procesar la solicitud de actualización llamando de nuevo a **OnLockGranted** con TS \_ LF \_ READWRITE.

## <a name="lock-enforcement"></a>Aplicación de bloqueos

La aplicación debe asegurarse de que existe el tipo de bloqueo adecuado antes de permitir el acceso al documento. Por ejemplo, la aplicación debe comprobar que un documento tiene al menos un bloqueo de solo lectura antes de permitir que [ITextStoreACP::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) o [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) continúen. Si no existe el bloqueo adecuado, la aplicación debe devolver TF \_ E \_ NOLOCK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Almacenes de texto](text-stores.md)
</dt> <dt>

[ITextStoreACP::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreACP::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




