---
title: Objeto de receptor de inserciones de escritor
description: Objeto de receptor de inserciones de escritor
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- SDK de Windows Media Format, objetos de receptor de extracción de escritor
- Advanced Systems Format (ASF), objetos de receptor de inserciones de escritor
- ASF (formato de sistemas avanzados), objetos de receptor de inserciones de escritor
- objetos, objetos de receptor de inserciones de escritor
- objetos de receptor de inserciones de escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994939"
---
# <a name="writer-push-sink-object"></a>Objeto de receptor de inserciones de escritor

El objeto de receptor de inserciones del escritor distribuye los medios digitales a los puntos de publicación. Por ejemplo, un concierto en directo se puede codificar mediante un solo servidor y, a continuación, entregarse o *insertarse* en otros servidores que realmente transmitirán el contenido a los usuarios.

La función [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)crea un objeto de receptor de inserciones de escritor, que establece un puntero a una interfaz **IWMWriterPushSink** . Las demás interfaces admitidas por el objeto, que se enumeran en la tabla siguiente, se pueden obtener llamando al método **QueryInterface** .



| Interfaz                                          | Descripción                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Permite que la aplicación obtenga mensajes de estado del objeto.                                                  |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | Administra una sesión de distribución de la extracción.                                                                             |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Asigna memoria, determina si el receptor está funcionando en tiempo real y expone varias funciones de devolución de llamada. |



 

La aplicación puede implementar la siguiente interfaz de devolución de llamada para realizar el seguimiento del progreso de un objeto de receptor de inserciones del escritor.



| Interfaz                                      | Descripción                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obligatorio cuando la información de estado se debe comunicar a la aplicación host. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Envío de datos ASF a un punto de publicación**](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




