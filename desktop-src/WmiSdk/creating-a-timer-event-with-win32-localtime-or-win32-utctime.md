---
description: Puede usar el modelo estándar de eventos intrínsecos y filtros de eventos en combinación con las clases Win32 LocalTime o Win32 UTCTime para recibir una notificación \_ \_ con tiempo.
ms.assetid: 89ba41e2-c9b5-4914-b8cb-13d21ff03402
ms.tgt_platform: multiple
title: Crear un evento de temporizador con Win32_LocalTime o Win32_UTCTime
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 011b2270a80f6b632e832f77e8e7c528228801b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170498"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a>Creación de un evento de temporizador con Win32 \_ LocalTime o Win32 \_ UTCTime

Puede usar el modelo estándar de eventos intrínsecos y filtros de eventos en combinación con las clases [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) para recibir una notificación con tiempo. El método intrínseco es una manera recomendada de generar eventos con tiempo, ya que es coherente con el resto del modelo de eventos de Microsoft y admite condiciones de programación complejas.

Las [**clases Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) y [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) son clases singleton en el espacio de nombres \\ raíz cimv2 que representan el reloj del sistema. Cuando se consulta, **Win32 \_ LocalTime** devuelve la hora actual en el momento de la recuperación de datos en un reloj de 24 horas con referencia local. La **clase \_ UTCTime de Win32** devuelve la hora actual con referencia UTC.

**Para generar eventos con tiempo o repeticiones con Win32 \_ LocalTime o Win32 \_ UTCTime**

-   Configure un filtro de eventos de notificación intrínseco para [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) que solicite notificación para una fecha y hora específicas.

Por ejemplo, si la hora local en Horario de verano es 4 p. m. y la ubicación es GMT -8, [**Win32 \_ LocalTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) devuelve 16 y [**Win32 \_ UTCTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) devuelve 23.

En el ejemplo de código siguiente se describe cómo crear un filtro de eventos que señale un evento repetido todos los días a medianoche.

``` syntax
// Win32_LocalTime and Win32_UTCTime reside in root\cimv2 namespace. 
// Defining the EventNamespace allows the filter
// to be compiled in any namespace.
instance of __EventFilter as $FILT1
{
 Name  = "wake-up call";
 Query = "SELECT * FROM __InstanceModificationEvent WHERE "    
 "TargetInstance ISA \"Win32_LocalTime\" AND "
 "TargetInstance.Hour = 0 AND TargetInstance.Minute = 0 AND "
 "TargetInstance.Second = 0";
 QueryLanguage = "WQL";
 EventNamespace = "root\\cimv2";
};
```

 

 
