---
title: Editar contextos
description: Editar contextos
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- Text Services Framework (TSF), editar contextos
- TSF (Text Services Framework), editar contextos
- servicios de texto, editar contextos
- Aplicaciones habilitadas para TSF, editar contextos
- editar contextos
- Text Services Framework (TSF), editar cookies
- TSF (Text Services Framework),editar cookies
- servicios de texto, editar cookies
- Aplicaciones habilitadas para TSF, editar cookies
- editar cookies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243662"
---
# <a name="edit-contexts"></a>Editar contextos

## <a name="applications"></a>Aplicaciones

Para crear un contexto de edición, una aplicación llama a [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).

## <a name="text-services"></a>Servicios de texto

Un servicio de texto suele utilizar el contexto de edición activo actualmente. El contexto de edición activo actualmente es el contexto de edición en la parte superior de la pila del administrador de documentos activo. Para obtener el contexto activo actualmente, un servicio de texto llama a [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) para obtener el administrador de documentos activo y, a continuación, llama a [ITfDocumentMgr::GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) para obtener el contexto de edición en la parte superior de la pila.

En algunos casos, un servicio de texto requiere su propio contexto de edición. Para crear un contexto de edición, un servicio de texto llama a **ITfDocumentMgr::CreateContext**.

## <a name="edit-cookies"></a>Editar cookies

Muchos métodos, como [ITfRange::SetText,](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)requieren una manera de identificar un contexto de edición que tenga un bloqueo de documento de solo lectura o de [lectura y escritura.](document-locks.md) Un bloqueo de documento se obtiene a través de una negociación entre el administrador de TSF y la aplicación. Un servicio de texto no puede realizar esta negociación directamente. Un servicio de texto solo puede [](edit-sessions.md) obtener un bloqueo solicitando una sesión de edición con un contexto específico y acceso de solo lectura o de lectura y escritura. Cuando se concede la sesión de edición, se proporciona al servicio de texto una *cookie de* edición que identifica el contexto de edición con el acceso solicitado. A continuación, esta cookie se pasa al método para identificar el contexto de edición con el acceso adecuado.

**ITfDocumentMgr::CreateContext** también proporciona una cookie de edición al creador del contexto. Esta cookie tiene acceso de solo lectura y no hay ninguna manera de modificar el nivel de acceso. En realidad, el administrador de TSF no negocia un bloqueo de documento para esta cookie de edición. La cookie se marca internamente como de solo lectura, pero el documento no está realmente bloqueado. Por ejemplo, si el creador del contexto llama a [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) con la cookie de edición devuelta por **ITfDocumentMgr::CreateContext** , se llama a [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) o [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) de la aplicación. Antes de obtener la selección, la aplicación determinará si existe un bloqueo de documento. Dado que no existe ningún bloqueo, se producirá un error en la aplicación con TS \_ E \_ NOLOCK. Es decir, si una aplicación llama a un método con esta cookie que da lugar a que se llame a uno de los métodos de almacén de texto de la aplicación, debe controlar este caso internamente porque la aplicación no tendrá realmente un bloqueo de documento.

Si el creador del contexto requiere una cookie de edición con acceso de lectura y escritura, debe establecer su propia sesión de edición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[ITfDocumentMgr::GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[Bloqueos de documentos](document-locks.md)
</dt> <dt>

[Sesiones de edición](edit-sessions.md)
</dt> <dt>

[ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




