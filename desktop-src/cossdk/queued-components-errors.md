---
description: Errores de componentes en cola
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Errores de componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714853"
---
# <a name="queued-components-errors"></a>Errores de componentes en cola

Cuando se produce un error en una llamada a un componente en cola, ya sea porque no se pudo transmitir al servidor (un error del lado cliente) o porque no se pudo ejecutar cuando llegó (un error del servidor), el mensaje de [Message Queue](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Server correspondiente recibe el nombre de mensaje *dudoso*.

El servicio de componentes en cola de COM+ controla los mensajes dudosos mediante una serie de colas de reintento. Después de varios reintentos, el mensaje se mueve a una cola de finalización. Los mensajes permanecen en la cola de permanencia hasta que se mueven manualmente mediante la utilidad del Movedor de mensajes de componentes en cola. Para obtener más información acerca del uso del Movedor de mensajes, consulte [control de errores](handling-errors-in-queued-components.md).

Puede encontrar descripciones detalladas de la secuencia de eventos que se produce para diversos tipos de errores en los temas que se describen en la tabla siguiente.



| Tema                                                                             | Descripción                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Errores del lado servidor](server-side-errors.md)<br/>                           | Describe en detalle la respuesta del servicio de componentes en cola de COM+ a un error del servidor.<br/>             |
| [Errores del lado cliente](client-side-errors.md)<br/>                           | Describe en detalle la respuesta del servicio de componentes en cola de COM+ a un error del lado cliente.<br/>             |
| [Errores de Client-Side persistentes](persistent-client-side-failures.md)<br/> | Describe en detalle la respuesta del servicio de componentes en cola de COM+ a errores repetidos del lado cliente.<br/> |



 

 

 




