---
description: Métodos de devolución de llamada asincrónicos
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Métodos de devolución de llamada asincrónicos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e59fec2423d6bc1b02a3f5ce05855419596bc92ea54062303ebd1315d087e489
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606715"
---
# <a name="asynchronous-callback-methods"></a>Métodos de devolución de llamada asincrónicos

Media Foundation proporciona una manera coherente de implementar métodos asincrónicos, mediante una interfaz de devolución de llamada.

En esta sección se describe cómo implementar la interfaz de devolución de llamada y cómo escribir métodos asincrónicos que usan esta interfaz. Contiene los temas siguientes.



| Tema                                                                                | Descripción                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Llamar a métodos asincrónicos](calling-asynchronous-methods.md)                     | Cómo llamar a métodos asincrónicos en Media Foundation.                                               |
| [Implementar la devolución de llamada asincrónica](implementing-the-asynchronous-callback.md) | Cómo implementar el método de devolución de llamada en la [**interfaz IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) |
| [Compatibilidad con varias devoluciones de llamada](supporting-multiple-callbacks.md)                   | Cómo admitir varias devoluciones de llamada dentro de la misma clase de C++.                                        |
| [Colas de trabajo](work-queues.md)                                                       | Las colas de trabajo proporcionan una manera eficaz de realizar operaciones asincrónicas en otro subproceso.          |
| [Escribir un método asincrónico](writing-an-asynchronous-method.md)                 | Cómo implementar métodos asincrónicos en Media Foundation.                                          |
| [Objetos de resultado asincrónico personalizados](custom-asynchronous-result-objects.md)         | Cómo proporcionar una implementación personalizada de la [**interfaz IMFAsyncResult.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**INTERFAZ DE DEVOLUCIÓN DE LLAMADA DE LA CLASE DE MÉTODOS DE DE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**Interfaz DENASYNCResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[Media Foundation API de plataforma](media-foundation-platform-apis.md)
</dt> </dl>

 

 



