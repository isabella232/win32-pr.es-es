---
description: Los mensajes de dispositivo son mensajes del sistema que notifican a las aplicaciones y otras características de eventos de cambio de dispositivo.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Mensajes del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164382"
---
# <a name="device-messages"></a>Mensajes del dispositivo

Los mensajes de dispositivo son mensajes del sistema que notifican a las aplicaciones y otras características de eventos de cambio de dispositivo. Estos eventos se producen siempre que el sistema detecta un cambio en el hardware del sistema, como cuando el usuario acopla y desacopla un equipo portátil, o inserta o quita un dispositivo como una tarjeta PCMCIA. Los eventos de dispositivo pueden producirse mientras el sistema se está ejecutando o cuando el sistema reanuda la operación después de suspenderse temporalmente.

Para ayudar a garantizar que las aplicaciones no pierden datos cuando los dispositivos no están disponibles, el sistema supervisa la configuración de hardware y envía mensajes de dispositivo a las aplicaciones para notificarles los cambios y darles la oportunidad de prepararse para los cambios antes de que se produzcan.

Para cada evento de dispositivo, el sistema difunde un [**mensaje \_ DEVICECHANGE de WM**](wm-devicechange.md) a todas las aplicaciones. En este mensaje, el *parámetro wParam* identifica el tipo de evento de dispositivo y el parámetro [](device-event-types.md) *lParam* es un puntero a datos específicos del evento.

 

 



