---
title: Usar el parámetro context
description: Usar el parámetro context
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows SDK de formato multimedia, parámetro de contexto
- Windows SDK de formato multimedia, parámetro pvContext
- Parámetro pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102315470243910158fd3bf474a209fa1e0888536671e3ede3764be519c672f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585205"
---
# <a name="using-the-context-parameter"></a>Usar el parámetro context

Algunas de las devoluciones de llamada usadas por Windows SDK de formato multimedia toman un parámetro denominado *pvContext*. Los objetos que llaman pasan a lo largo del valor especificado en el método que inició la acción asincrónica. Por ejemplo, cuando se llama a [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), se puede pasar un valor para *pvContext*. Cuando el objeto lector llama al método [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) para notificar a la aplicación que el archivo se ha abierto, pasará el valor que usó en la llamada a **Open** como parámetro *pvContext* de **OnStatus.** Este parámetro de contexto se proporciona para su uso y puede usarlo de la manera que quiera.

El *parámetro pvContext se* usa con mayor frecuencia cuando varios objetos necesitan compartir la misma devolución de llamada. Por ejemplo, varios objetos usan el [**método IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Puede usar *pvContext para permitir* que los distintos objetos compartan una implementación de **OnStatus** pasando un valor diferente para *pvContext* en la llamada original. En la implementación de **OnStatus**, puede bifurcar la lógica de control de mensajes en función del valor de *pvContext*.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar los métodos de devolución de llamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




