---
title: Administrador de documentos
description: Administrador de documentos
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- Marco de trabajo de servicios de texto (TSF), administrador de documentos
- TSF (marco de trabajo de servicios de texto), administrador de documentos
- servicios de texto, administrador de documentos
- Aplicaciones habilitadas para TSF, administrador de documentos
- Administrador de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774449"
---
# <a name="document-manager"></a>Administrador de documentos

## <a name="applications"></a>APLICACIONES

Para crear un objeto de administrador de documentos, una aplicación llama a [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr). La aplicación crea un objeto de administrador de documentos independiente para cada documento individual que mantiene la aplicación. La aplicación utiliza el administrador de documentos para crear contextos de edición, agregar un contexto a la pila de contexto y quitar un contexto de la pila de contexto.

## <a name="text-services"></a>Servicios de texto

Un servicio de texto nunca crea un objeto de administrador de documentos. En su lugar, el servicio de texto obtiene el objeto actual del administrador de documentos mediante una llamada a [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus). Un servicio de texto utiliza el administrador de documentos para obtener el contexto en la parte superior de la pila.

Un servicio de texto también puede usar el administrador de documentos para crear su propio contexto y agregarlo y quitarlo de la pila de contexto. Normalmente, esto se hace cuando el servicio de texto debe mostrar alguna interfaz de usuario modal, como cuando se muestra una lista de palabras para permitir al usuario seleccionar una palabra. Cuando se muestra la lista, el servicio de texto coloca su propio contexto en la pila. Cuando se descarta la lista de palabras, el servicio de texto quita su contexto de la pila.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




