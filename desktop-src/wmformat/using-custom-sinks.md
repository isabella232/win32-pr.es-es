---
title: Usar receptores personalizados
description: Usar receptores personalizados
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- Advanced Systems Format (ASF), receptores personalizados
- ASF (formato de sistemas avanzados), receptores personalizados
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- receptores, receptores personalizados
- receptores personalizados, acerca de
- receptores de escritor, receptores personalizados
- receptores personalizados, interfaz IWMWriterSink
- IWMWriterSink
- receptores de escritor, interfaz IWMWriterSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788751"
---
# <a name="using-custom-sinks"></a>Usar receptores personalizados

Si tiene una necesidad especial de escritura, puede crear sus propios receptores de escritor. El sistema de escritura mantiene la comunicación unidireccional con un receptor realizando llamadas a los métodos de [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink). Para crear su propio receptor, implemente la interfaz **IWMWriterSink** en una clase de la aplicación. Este proceso es muy similar a la implementación de cualquier otra interfaz de devolución de llamada utilizada por los objetos del SDK de Windows Media Format. Para obtener más información sobre las devoluciones de llamada, vea [usar los métodos de devolución de llamada](using-the-callback-methods.md).

El búfer recibido en [**IWMWriterSink:: MyHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) debe escribirse en el principio del archivo y todos los búferes recibidos en [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) se deben escribir secuencialmente. Se llama al método **MyHeader** al principio, pero también se le puede llamar en otros momentos, y si es así, debe sobrescribir el encabezado original, si es posible. Si, por algún motivo, la aplicación no puede realizar esta tarea, simplemente omita las llamadas de un **subcabezal** posteriores.

El receptor personalizado debe comunicar su estado a la aplicación de escritura realizando llamadas al método de devolución de llamada [**IWMStatusCallback:: Alstatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Si implementa el receptor como un objeto COM, es posible que desee exponer la interfaz [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) . Sin embargo, puede pasar la dirección de la devolución de llamada de **Estado** al receptor y establecer un contexto de la forma que desee.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




