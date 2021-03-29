---
title: Identificadores de cliente
description: Identificadores de cliente
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- Text Services Framework (TSF), identificadores de cliente
- TSF (marco de trabajo de servicios de texto), identificadores de cliente
- servicios de texto, identificadores de cliente
- Aplicaciones habilitadas para TSF, identificadores de cliente
- identificadores de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de15b208d2fbc6c6ea5c2a1114eb5cb23ff12ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994045"
---
# <a name="client-identifiers"></a>Identificadores de cliente

## <a name="applications"></a>APLICACIONES

Una aplicación obtiene su identificador de cliente mediante una llamada a [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).

## <a name="text-services"></a>Servicios de texto

Un servicio de texto obtiene su identificador de cliente cuando se llama al método [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) del servicio de texto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




