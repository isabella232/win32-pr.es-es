---
title: Administrador de documentos
description: Administrador de documentos
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- Text Services Framework (TSF), administrador de documentos
- TSF (Text Services Framework),administrador de documentos
- servicios de texto, administrador de documentos
- Aplicaciones habilitadas para TSF, administrador de documentos
- administrador de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dc0633ed63d542926657481e673481fd35472c12b316b98bfd1d77053d5c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118879709"
---
# <a name="document-manager"></a>Administrador de documentos

## <a name="applications"></a>Aplicaciones

Para crear un objeto de administrador de documentos, una aplicación llama [a ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr). La aplicación crea un objeto de administrador de documentos independiente para cada documento individual que mantiene la aplicación. La aplicación usa el administrador de documentos para crear contextos de edición, agregar un contexto a la pila de contexto y quitar un contexto de la pila de contextos.

## <a name="text-services"></a>Servicios de texto

Un servicio de texto nunca crea un objeto de administrador de documentos. En su lugar, el servicio de texto obtiene el objeto de administrador de documentos activo actualmente llamando a [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus). Un servicio de texto usa el administrador de documentos para obtener el contexto en la parte superior de la pila.

Un servicio de texto también puede usar el administrador de documentos para crear su propio contexto y agregarlo y quitarlo de la pila de contexto. Normalmente, esto se hace cuando el servicio de texto debe mostrar alguna interfaz de usuario modal, por ejemplo, cuando se muestra una lista de palabras para permitir que el usuario seleccione una palabra. Cuando se muestra la lista, el servicio de texto coloca su propio contexto en la pila. Cuando se descarta la lista de palabras, el servicio de texto quita su contexto de la pila.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




