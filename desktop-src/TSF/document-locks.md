---
title: Bloqueos de documento
description: Bloqueos de documento
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- Marco de trabajo de servicios de texto (TSF), bloqueos de documento
- TSF (marco de trabajo de servicios de texto), bloqueos de documento
- Aplicaciones habilitadas para TSF, bloqueos de documentos
- bloqueos de documento
- Marco de trabajo de servicios de texto (TSF), posición de caracteres de aplicación (ACP)
- TSF (marco de trabajo de servicios de texto), posición de carácter de aplicación (ACP)
- Aplicaciones habilitadas para TSF, posición de caracteres de aplicación (ACP)
- Posición de carácter de aplicación (ACP)
- ACP (posición de carácter de aplicación)
- Text Services Framework (TSF), delimitadores
- TSF (marco de trabajo de servicios de texto), delimitadores
- Aplicaciones habilitadas para TSF, delimitadores
- delimitadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268529"
---
# <a name="document-locks"></a>Bloqueos de documento

## <a name="the-document-lock-protocol"></a>Protocolo de bloqueo de documento

Para solicitar un bloqueo de documento para aplicaciones basadas en ACP, el administrador de TSF llama a [ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock). En el caso de las aplicaciones basadas en delimitadores, el administrador de TSF llama a [ITextStoreAnchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock). La aplicación concede el bloqueo del documento mediante una llamada a [ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (aplicaciones basadas en ACP) o [ITextStoreAnchorSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (aplicaciones basadas en delimitadores) dentro de **RequestLock**. El bloqueo solo es válido durante la llamada a **OnLockGranted** . Cuando **OnLockGranted** devuelve, el documento se considera desbloqueado.

## <a name="types-of-document-locks"></a>Tipos de bloqueos de documento

Hay dos tipos de bloqueos de documento, de solo lectura y de lectura/escritura. Un bloqueo de solo lectura permite al administrador leer el texto, pero no puede modificar ni insertar texto. Un bloqueo de lectura/escritura permite al administrador leer, modificar e insertar texto. Se solicita un bloqueo de solo lectura mediante la especificación \_ de la \_ lectura de LF de TS en *dwFlags*. Se solicita un bloqueo de lectura/escritura especificando TS \_ LF \_ ReadWrite en *dwFlags*.

## <a name="asynchronous-and-synchronous-requests"></a>Solicitudes asincrónicas y sincrónicas

Una solicitud de bloqueo puede ser sincrónica o asincrónica. El administrador solicita un bloqueo sincrónico mediante el uso de la \_ \_ marca de sincronización LF de TS en *dwFlags*. Si este marcador no está presente, la solicitud es asincrónica.

## <a name="granting-the-lock"></a>Concesión del bloqueo

Cuando se llama a **RequestLock** , la aplicación debe determinar si el documento está bloqueado actualmente. Si el documento no está bloqueado y no existe ningún otro motivo para denegar el bloqueo, la aplicación debe establecer *phrSession* en S \_ OK y devolver S \_ OK.

Si el documento está bloqueado y la solicitud de bloqueo es sincrónica, la aplicación debe establecer *phrSession* en TS \_ e \_ sincrónico y devolver S \_ correcto. Esto indica que no se puede conceder una solicitud sincrónica.

Si el documento está bloqueado y la solicitud de bloqueo es asincrónica, la aplicación debe poner en cola la solicitud, establecer *phrSession* en TS \_ S \_ Async y devolver s \_ OK. Cuando el documento esté disponible, la aplicación debe quitar la solicitud de la cola y llamar a **OnLockGranted**. Esta cola de solicitudes de bloqueo es opcional. hay un escenario que una aplicación debe admitir. Si el documento tiene un bloqueo de solo lectura, la nueva solicitud de bloqueo es de lectura y escritura y la solicitud es asincrónica, la aplicación ha llamado a **OnLockGranted** , lo que ha provocado una llamada reentrante a **RequestLock**. La aplicación debe establecer *phrSession* en TS \_ s \_ Async y devolver s \_ OK. Después de que la llamada a **OnLockGranted** devuelva, la aplicación debe procesar la solicitud de actualización mediante una llamada a **OnLockGranted** de nuevo con TS \_ LF \_ ReadWrite.

## <a name="lock-enforcement"></a>Aplicación de bloqueos

La aplicación debe asegurarse de que existe el tipo de bloqueo adecuado antes de permitir el acceso al documento. Por ejemplo, la aplicación debe comprobar que un documento tiene al menos un bloqueo de solo lectura antes de permitir [ITextStoreACP:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) o [ITextStoreAnchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) para continuar. Si el bloqueo adecuado no existe, la aplicación debe devolver TF \_ E \_ NOLOCK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Almacenes de texto](text-stores.md)
</dt> <dt>

[ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreACP:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[ITextStoreAnchor:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




