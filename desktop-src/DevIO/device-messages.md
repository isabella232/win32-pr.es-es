---
description: Los mensajes de dispositivo son mensajes del sistema que notifican a las aplicaciones y otras características de los eventos de cambio de dispositivo.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Mensajes del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659665"
---
# <a name="device-messages"></a>Mensajes del dispositivo

Los mensajes de dispositivo son mensajes del sistema que notifican a las aplicaciones y otras características de los eventos de cambio de dispositivo. Estos eventos se producen siempre que el sistema detecta un cambio en el hardware del sistema, por ejemplo, cuando el usuario acopla y desacopla un equipo portátil, o inserta o quita un dispositivo como una tarjeta PCMCIA. Los eventos de dispositivo pueden producirse mientras el sistema se está ejecutando o cuando el sistema reanuda la operación después de suspenderse temporalmente.

Para asegurarse de que las aplicaciones no pierdan datos cuando los dispositivos dejen de estar disponibles, el sistema supervisa la configuración de hardware y envía mensajes de dispositivo a las aplicaciones para notificar los cambios y dar la oportunidad de prepararse para los cambios antes de que se produzcan.

Para cada evento de dispositivo, el sistema difunde un mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) a todas las aplicaciones. En este mensaje, el parámetro *wParam* identifica el [tipo de evento de dispositivo](device-event-types.md) y el parámetro *lParam* es un puntero a datos específicos del evento.

 

 



