---
description: Mensajes de calidad
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Mensajes de calidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537149"
---
# <a name="quality-messages"></a>Mensajes de calidad

Los mensajes de calidad se definen con la estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) . Esta estructura contiene los siguientes miembros:

-   **Tipo:** Definido por la enumeración [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) ; Famine, que indica que el filtro está recibiendo demasiados datos, o inundaciones, que indican que el filtro está recibiendo demasiados datos.
-   **Proporción:** Ajuste solicitado en la velocidad de datos, de una línea base de 1000. Por ejemplo, 750 indica 75% y 1500 indica 150%.
-   **Tardía:** Tiempo de referencia que indica en qué momento llegó la muestra más reciente. El valor es negativo si el ejemplo llegó pronto.
-   **Marca** de tiempo: Marca de tiempo de la muestra más reciente.

Por ejemplo, supongamos que un ejemplo con una marca de tiempo de 240 milisegundos (MS) alcanza el representador en 280 MS, tiempo de secuencia. El representador crea un mensaje de calidad de tipo Famine. El ejemplo llegó a 40 ms en tiempo de espera, por lo que el **último** miembro es 400000. (Todos los tiempos de referencia están en unidades de 100 a nanosegundos). El miembro **timestamp** es 2,4 millones.

En el caso del miembro **proporcional** , el representador podría usar un promedio de ejecución para calcular el valor. Es posible que las muestras hayan llegado a tiempo y este ejemplo sea una anomalía. En ese caso, es posible que el representador solicite solo una pequeña corrección. Por otro lado, si las muestras se atrasan constantemente, el representador podría solicitar una corrección mayor.

El control de calidad se controla a través de la interfaz [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) . Contiene dos métodos.

-   [**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): envía un mensaje de calidad.
-   [**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): especifica un administrador de calidad personalizado.

Un objeto que implementa **IQualityControl** recibe mensajes de calidad a través de su método **Notify** . Puede controlar el mensaje o pasar el mensaje a otro objeto. Si la aplicación llama al método **SetSink** del objeto, el objeto debe delegar el control de calidad al administrador de calidad especificado.

 

 



