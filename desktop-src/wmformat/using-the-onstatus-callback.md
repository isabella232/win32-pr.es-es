---
title: Usar la devolución de llamada en estado
description: Usar la devolución de llamada en estado
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- SDK de Windows Media Format, método de devolución de llamada de estado
- SDK de Windows Media Format, interfaz IWMStatusCallback
- Método de devolución de llamada de estado, acerca de
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994926"
---
# <a name="using-the-onstatus-callback"></a>Usar la devolución de llamada en estado

Varios objetos del SDK de formato de Windows Media llaman al método de devolución de llamada [**IWMStatusCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) OnFormat. En **Estado** recibe mensajes que representan cambios en el estado de las operaciones del SDK.

Para usar el método de devolución de llamada en **Estado** , debe implementar una clase en la aplicación que herede de la interfaz [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) . Incluya código para su versión de en **Estado** en la clase. En los ejemplos incluidos con este SDK se pueden encontrar varios ejemplos de implementaciones de **Estado** . Para obtener más información acerca de los ejemplos, vea [aplicaciones de ejemplo](sample-applications.md).

Debe asociar la implementación de la devolución de llamada de estado con varios objetos del SDK de Windows Media Format. Cada objeto tiene una forma diferente de crear esta asociación. Para obtener una lista de los métodos que asocian objetos específicos, vea la página de referencia de **IWMStatusCallback** .

Los mensajes de estado que se pueden recibir en **Estado** se definen en el tipo de enumeración [**\_ Estado de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .

Puede elegir qué mensajes desea interceptar y qué omitir. Sin embargo, es necesario responder a algunos mensajes de estado para determinadas características. Por ejemplo, al usar el lector asincrónico, el método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) abre un archivo de forma asincrónica. La única forma de saber cuándo se ha abierto el archivo es atrapar el \_ mensaje abierto de MWT. Normalmente, los mensajes a los que responde son notificaciones de la finalización de las tareas asincrónicas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar los métodos de devolución de llamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




