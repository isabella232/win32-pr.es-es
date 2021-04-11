---
title: Usar el parámetro de contexto
description: Usar el parámetro de contexto
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- SDK de Windows Media Format, parámetro de contexto
- SDK de Windows Media Format, parámetro pvContext
- parámetro pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149074"
---
# <a name="using-the-context-parameter"></a>Usar el parámetro de contexto

Algunas de las devoluciones de llamada utilizadas por el SDK de Windows Media Format toman un parámetro denominado *pvContext*. Los objetos de llamada pasan a lo largo del valor especificado en el método que inició la acción asincrónica. Por ejemplo, al llamar a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), puede pasar un valor para *pvContext*. Cuando el objeto de lector llama al método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) para notificar a la aplicación que el archivo se ha abierto, pasará cualquier valor que se haya usado en la llamada a **Open** como el parámetro *pvContext* de en **status**. Este parámetro de contexto se proporciona para su uso y puede usarlo de la forma que desee.

Normalmente, el parámetro *pvContext* se usa cuando es necesario que varios objetos compartan la misma devolución de llamada. Por ejemplo, varios objetos usan el método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Puede usar *pvContext* para permitir que los distintos objetos compartan una implementación de en **Estado** pasando un valor diferente para *pvContext* en la llamada original. En la implementación de en el **Estado**, puede crear una bifurcación de la lógica de control de mensajes basada en el valor de *pvContext*.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar los métodos de devolución de llamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




