---
title: Uso de la devolución de llamada OnStatus
description: Uso de la devolución de llamada OnStatus
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows SDK de formato multimedia, método de devolución de llamada OnStatus
- Windows SDK de formato multimedia, interfaz IWMStatusCallback
- Método de devolución de llamada OnStatus,about
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466472"
---
# <a name="using-the-onstatus-callback"></a>Uso de la devolución de llamada OnStatus

Varios objetos del SDK de Windows multimedia llaman al método de devolución de llamada [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) **OnStatus** recibe mensajes que representan los cambios en el estado de las operaciones del SDK.

Para usar el método de devolución de llamada **OnStatus,** debe implementar una clase en la aplicación que herede de la [**interfaz IWMStatusCallback.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) Incluya código para la versión de **OnStatus** en la clase . Puede encontrar varios **ejemplos de implementaciones de OnStatus** en los ejemplos incluidos con este SDK. Para obtener más información sobre los ejemplos, vea [Aplicaciones de ejemplo](sample-applications.md).

Debe asociar la implementación de la devolución de llamada de estado con varios objetos del SDK Windows Media Format. Cada objeto tiene una manera diferente de realizar esta asociación. Para obtener una lista de los métodos que asocian objetos específicos, vea la página de **referencia de IWMStatusCallback.**

Los mensajes de estado que puede recibir **OnStatus** se definen en el tipo [**de enumeración WMT \_ STATUS.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)

Puede elegir qué mensajes se capturan y cuáles se omitirán. Sin embargo, es necesario responder a algunos mensajes de estado para determinadas características. Por ejemplo, cuando se usa el lector asincrónico, el [**método IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) abre un archivo de forma asincrónica. La única manera de saber cuándo se ha abierto el archivo es capturar el mensaje DE LA \_ VENTANA ABIERTA. Normalmente, los mensajes a los que responde son notificaciones de la finalización de tareas asincrónicas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar los métodos de devolución de llamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




