---
description: Mensajes de calidad
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Mensajes de calidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15224e147d363a6cf3f3a55971d35a3d6596d95f07b9897ab1f258cc7febad48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747705"
---
# <a name="quality-messages"></a>Mensajes de calidad

Los mensajes de calidad se definen con la [**estructura Calidad.**](/windows/win32/api/strmif/ns-strmif-quality) Esta estructura contiene los miembros siguientes:

-   **Tipo:** Definido por la [**enumeración QualityMessageType;**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) O bien Flejos, que indica que el filtro recibe demasiados datos, o Flood, que indica que el filtro recibe demasiados datos.
-   **Proporción:** Ajuste solicitado en la velocidad de datos, a partir de una línea base de 1000. Por ejemplo, 750 indica 75 % y 1500 indica 150 %.
-   **Tarde:** Tiempo de referencia que indica la hora de llegada de la muestra más reciente. El valor es negativo si la muestra llegó pronto.
-   **TimeStamp:** Marca de tiempo del ejemplo más reciente.

Por ejemplo, suponga que una muestra con una marca de tiempo de 240 milisegundos (ms) llega al representador a 280 ms, tiempo de transmisión. El representador crea un mensaje de calidad de tipo Fmino. El ejemplo llegó 40 ms tarde, por lo que el **miembro Late** es 400000. (Todos los tiempos de referencia están en unidades de 100 nanosegundos). El **miembro TimeStamp** es 2400000.

Para el **miembro Proportion,** el representador podría usar un promedio de ejecución para calcular el valor. Quizás los ejemplos han llegado a tiempo y este ejemplo es una anomalía. En ese caso, el representador podría solicitar solo una pequeña corrección. Por otro lado, si las muestras se retrasan constantemente, el representador podría solicitar una corrección mayor.

El control de calidad se controla a través de [**la interfaz IQualityControl.**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) Contiene dos métodos.

-   [**Notificar:**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)envía un mensaje de calidad.
-   [**SetSink:**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)especifica un administrador de calidad personalizado.

Un objeto que implementa **IQualityControl recibe** mensajes de calidad a través de su **método Notify.** Puede controlar el mensaje o pasarlo a otro objeto. Si la aplicación llama al método **SetSink del** objeto, el objeto debe delegar el control de calidad en el administrador de calidad especificado.

 

 



