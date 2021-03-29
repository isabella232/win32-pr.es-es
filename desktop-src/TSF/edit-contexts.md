---
title: Editar contextos
description: Editar contextos
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- Marco de trabajo de servicios de texto (TSF), editar contextos
- TSF (marco de trabajo de servicios de texto), editar contextos
- servicios de texto, editar contextos
- Aplicaciones habilitadas para TSF, editar contextos
- Editar contextos
- Marco de trabajo de servicios de texto (TSF), editar cookies
- TSF (marco de trabajo de servicios de texto), editar cookies
- servicios de texto, editar cookies
- Aplicaciones habilitadas para TSF, editar cookies
- Editar cookies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903373"
---
# <a name="edit-contexts"></a>Editar contextos

## <a name="applications"></a>APLICACIONES

Para crear un contexto de edición, una aplicación llama a [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).

## <a name="text-services"></a>Servicios de texto

A menudo, un servicio de texto utiliza el contexto de edición actualmente activo. El contexto de edición actualmente activo es el contexto de edición situado en la parte superior de la pila del administrador de documentos activo. Para obtener el contexto activo actualmente, un servicio de texto llama a [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) para obtener el administrador de documentos activo y, a continuación, llama a [ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) para obtener el contexto de edición en la parte superior de la pila.

En algunos casos, un servicio de texto requiere su propio contexto de edición. Para crear un contexto de edición, un servicio de texto llama a **ITfDocumentMgr:: CreateContext**.

## <a name="edit-cookies"></a>Editar cookies

Muchos métodos, como [ITfRange:: setText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), requieren una manera de identificar un contexto de edición que tiene un [bloqueo de documento](document-locks.md)de solo lectura o de lectura y escritura. Se obtiene un bloqueo de documento a través de una negociación entre el administrador de TSF y la aplicación. Un servicio de texto no puede realizar esta negociación directamente. Un servicio de texto solo puede obtener un bloqueo solicitando una [sesión de edición](edit-sessions.md) con un contexto específico y acceso de solo lectura o de lectura y escritura. Cuando se concede la sesión de edición, el servicio de texto se proporciona con una *cookie de edición* que identifica el contexto de edición con el acceso solicitado. A continuación, esta cookie se pasa al método para identificar el contexto de edición con el acceso adecuado.

**ITfDocumentMgr:: CreateContext** también proporciona una cookie de edición para el creador del contexto. Esta cookie tiene acceso de solo lectura y no hay ninguna manera de modificar el nivel de acceso. En realidad, el administrador de TSF no negocia un bloqueo de documento para esta cookie de edición. La cookie está marcada internamente como de solo lectura, pero el documento no está realmente bloqueado. Por ejemplo, si el creador de contexto llama a [ITfContext:: getSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) con la cookie de edición devuelta por **ITfDocumentMgr:: CreateContext** , esto da como resultado la llamada a [ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) o [ITextStoreAnchor:: getSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) de la aplicación. Antes de obtener la selección, la aplicación determinará si existe un bloqueo de documento. Dado que no existe ningún bloqueo, se producirá un error en la aplicación con el bloqueo de TS \_ E \_ . Es decir, si una aplicación llama a un método con esta cookie que da como resultado la llamada a uno de los métodos del almacén de texto de la aplicación, debe tratar este caso internamente porque la aplicación no tendrá realmente un bloqueo del documento.

Si el creador del contexto requiere una cookie de edición con acceso de lectura y escritura, debe establecer su propia sesión de edición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[Bloqueos de documento](document-locks.md)
</dt> <dt>

[Sesiones de edición](edit-sessions.md)
</dt> <dt>

[ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




