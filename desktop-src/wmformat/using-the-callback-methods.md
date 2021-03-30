---
title: Usar los métodos de devolución de llamada
description: Usar los métodos de devolución de llamada
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- SDK de Windows Media Format, métodos de devolución de llamada
- SDK de Windows Media Format, métodos denominados de forma asincrónica
- métodos de devolución de llamada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788703"
---
# <a name="using-the-callback-methods"></a>Usar los métodos de devolución de llamada

Varias interfaces del SDK de Windows Media Format contienen métodos a los que se llama de forma asincrónica. La mayoría de estos métodos usan funciones de devolución de llamada para pasar información a la aplicación de control.

En las secciones siguientes se describen algunos de los problemas generales relacionados con el uso de métodos de devolución de llamada con el SDK de Windows Media Format.



| Sección                                                                          | Descripción                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Usar la devolución de llamada en estado](using-the-onstatus-callback.md)                   | Describe cómo implementar el método de devolución de llamada [**IWMStatusCallback:: Alstatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , que utilizan varios objetos para notificar a las aplicaciones el progreso de la operación del SDK. |
| [Usar eventos con llamadas asincrónicas](using-events-with-asynchronous-calls.md) | Describe una técnica común para controlar las llamadas a métodos asincrónicos en una aplicación.                                                                                                                  |
| [Usar el parámetro de contexto](using-the-context-parameter.md)                   | Presenta el parámetro *pvContext* , compartido por varias devoluciones de llamada y sus métodos de llamada, y explica cómo utilizarla.                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 




