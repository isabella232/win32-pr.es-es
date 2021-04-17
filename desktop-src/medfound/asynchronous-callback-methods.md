---
description: Métodos de devolución de llamada asincrónica
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Métodos de devolución de llamada asincrónica
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705429"
---
# <a name="asynchronous-callback-methods"></a>Métodos de devolución de llamada asincrónica

Media Foundation proporciona una manera coherente de implementar métodos asincrónicos, mediante una interfaz de devolución de llamada.

En esta sección se describe cómo implementar la interfaz de devolución de llamada y cómo escribir métodos asincrónicos que usan esta interfaz. Contiene los temas siguientes.



| Tema                                                                                | Descripción                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Llamar a métodos asincrónicos](calling-asynchronous-methods.md)                     | Cómo llamar a métodos asincrónicos en Media Foundation.                                               |
| [Implementar la devolución de llamada asincrónica](implementing-the-asynchronous-callback.md) | Cómo implementar el método de devolución de llamada en la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . |
| [Admitir varias devoluciones de llamada](supporting-multiple-callbacks.md)                   | Cómo admitir varias devoluciones de llamada dentro de la misma clase de C++.                                        |
| [Colas de trabajo](work-queues.md)                                                       | Las colas de trabajo proporcionan una manera eficaz de realizar operaciones asincrónicas en otro subproceso.          |
| [Escribir un método asincrónico](writing-an-asynchronous-method.md)                 | Cómo implementar métodos asincrónicos en Media Foundation.                                          |
| [Objetos de resultado asincrónicos personalizados](custom-asynchronous-result-objects.md)         | Cómo proporcionar una implementación personalizada de la interfaz [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**Interfaz IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[API de Media Foundation Platform](media-foundation-platform-apis.md)
</dt> </dl>

 

 



