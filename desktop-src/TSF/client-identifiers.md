---
title: Identificadores de cliente
description: Identificadores de cliente
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- Text Services Framework (TSF),identificadores de cliente
- TSF (Text Services Framework),identificadores de cliente
- servicios de texto, identificadores de cliente
- Aplicaciones habilitadas para TSF, identificadores de cliente
- identificadores de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f37b230eed1f47ad3e31a5831bddaf8634837c1173806deb084c1e3a4d08790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117953913"
---
# <a name="client-identifiers"></a>Identificadores de cliente

## <a name="applications"></a>Aplicaciones

Una aplicación obtiene su identificador de cliente llamando a [ITfThreadMgr::Activate.](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)

## <a name="text-services"></a>Servicios de texto

Un servicio de texto obtiene su identificador de cliente cuando se llama al método [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) del servicio de texto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




