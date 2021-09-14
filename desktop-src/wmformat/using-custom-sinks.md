---
title: Uso de receptores personalizados
description: Uso de receptores personalizados
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- Formato de sistemas avanzados (ASF), receptores personalizados
- ASF (formato de sistemas avanzados), receptores personalizados
- Formato de sistemas avanzados (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- sinks,custom sinks
- receptores personalizados, acerca de
- receptores de escritor, receptores personalizados
- receptores personalizados, interfaz IWMWriterSink
- IWMWriterSink
- receptores de escritor, interfaz IWMWriterSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359558"
---
# <a name="using-custom-sinks"></a>Uso de receptores personalizados

Si tiene una necesidad especial de escritura, puede crear sus propios receptores de escritor. El sistema de escritura mantiene la comunicación unida con un receptor mediante llamadas a los métodos de [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink). Para crear su propio receptor, implemente la **interfaz IWMWriterSink** en una clase de la aplicación. Este proceso es muy similar a implementar cualquier otra interfaz de devolución de llamada utilizada por los objetos del SDK Windows Media Format. Para obtener más información sobre las devoluciones de llamada, vea [Usar los métodos de devolución de llamada](using-the-callback-methods.md).

El búfer recibido en [**IWMWriterSink::OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) debe escribirse al principio del archivo y todos los búferes recibidos en [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) deben escribirse secuencialmente. **Se llamará** a OnHeader al principio, pero también se le podría llamar en otras ocasiones y, si es así, debe sobrescribir, si es posible, el encabezado original. Si la aplicación no puede hacerlo por alguna razón, simplemente ignore las llamadas **OnHeader** posteriores.

El receptor personalizado debe comunicar su estado a la aplicación de escritura mediante llamadas al método de devolución de llamada [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Si implementa el receptor como un objeto COM, puede exponer la [**interfaz IWMRegisterCallback.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) Sin embargo, puede pasar la dirección de la devolución de llamada **OnStatus** al receptor y establecer un contexto de la manera que quiera.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




