---
description: Métodos de devolución de llamada asincrónicos
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Métodos de devolución de llamada asincrónicos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361179"
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

[**INTERFAZ DE DEVOLUCIÓNASYNCCALLBACK**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**INTERFAZ DESASYNCRESULT**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[Media Foundation API de plataforma de aplicaciones](media-foundation-platform-apis.md)
</dt> </dl>

 

 



