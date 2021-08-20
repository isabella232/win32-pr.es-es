---
title: Objeto receptor de inserción de escritor
description: Objeto receptor de inserción de escritor
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows SDK de formato multimedia, objetos receptores de inserción de escritor
- Formato de sistemas avanzados (ASF), escribir objetos receptores de inserción
- ASF (formato de sistemas avanzados), escritura de objetos receptores de inserción
- objects,writer push sink objects
- objetos de receptor de inserción de escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859e4d2d5cf2530e655b74705b1d6f9ef93960d28f523c00e0da7a7336ab258d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006335"
---
# <a name="writer-push-sink-object"></a>Objeto receptor de inserción de escritor

El objeto receptor de inserción de escritor distribuye los medios digitales a los puntos de publicación. Por ejemplo, un solo servidor puede codificar un directo y, a continuación, entregarlo o insertarlo en otros servidores que transmitirán realmente el contenido a los usuarios.

La función [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)crea un objeto receptor de inserción de escritor, que establece un puntero a una **interfaz IWMWriterPushSink.** Las demás interfaces admitidas por el objeto , enumeradas en la tabla siguiente, se pueden obtener llamando al **método QueryInterface.**



| Interfaz                                          | Descripción                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Permite que la aplicación obtenga mensajes de estado del objeto .                                                  |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | Administra una sesión de distribución de inserción.                                                                             |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Asigna memoria, determina si el receptor funciona en tiempo real y expone varias funciones de devolución de llamada. |



 

La aplicación puede implementar la siguiente interfaz de devolución de llamada para realizar un seguimiento del progreso de un objeto receptor de inserción de escritor.



| Interfaz                                      | Descripción                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Se requiere cuando se debe comunicar la información de estado a la aplicación host. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Envío de datos de ASF a un punto de publicación**](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




