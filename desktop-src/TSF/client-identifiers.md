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
ms.openlocfilehash: 9de15b208d2fbc6c6ea5c2a1114eb5cb23ff12ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243711"
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

 

 




