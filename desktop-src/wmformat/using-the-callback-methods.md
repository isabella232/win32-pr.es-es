---
title: Usar los métodos de devolución de llamada
description: Usar los métodos de devolución de llamada
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows SDK de formato multimedia, métodos de devolución de llamada
- Windows SDK de formato multimedia, métodos a los que se llama de forma asincrónica
- métodos de devolución de llamada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ee2bcf6587e2e9e75e18404a60c3b85fb4bac5e9f14fd0164304bcc3f3338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110065"
---
# <a name="using-the-callback-methods"></a>Usar los métodos de devolución de llamada

Varias interfaces del SDK Windows Media Format contienen métodos a los que se llama de forma asincrónica. La mayoría de estos métodos usan funciones de devolución de llamada para pasar información a la aplicación de control.

En las secciones siguientes se describen algunos de los problemas generales relacionados con el uso de métodos de devolución de llamada con el SDK Windows Media Format.



| Sección                                                                          | Descripción                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uso de la devolución de llamada OnStatus](using-the-onstatus-callback.md)                   | Describe cómo implementar el método de devolución de llamada [**IWMStatusCallback::OnStatus,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) que usan varios objetos para aconsejar a las aplicaciones el progreso de la operación del SDK. |
| [Uso de eventos con llamadas asincrónicas](using-events-with-asynchronous-calls.md) | Describe una técnica común para controlar las llamadas a métodos asincrónicos en una aplicación.                                                                                                                  |
| [Usar el parámetro context](using-the-context-parameter.md)                   | Presenta el parámetro *pvContext,* compartido por varias devoluciones de llamada y sus métodos de llamada, y explica cómo usarlo.                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 




