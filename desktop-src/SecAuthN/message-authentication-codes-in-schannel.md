---
description: Se usa un código de autenticación de mensajes (MAC) para detectar la manipulación y falsificación de mensajes.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Códigos de autenticación de mensajes en Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db81efbaa71dc94094e5efb14d11dde600798cc8f58855a3a3ae116a624b679f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786987"
---
# <a name="message-authentication-codes-in-schannel"></a>Códigos de autenticación de mensajes en Schannel

Se [*usa un código de autenticación*](../secgloss/m-gly.md) de mensajes (MAC) para detectar la manipulación y falsificación de mensajes. El remitente de un mensaje crea un MAC mediante el cifrado [](../secgloss/s-gly.md) de un [*hash*](../secgloss/h-gly.md) unitorio del cuerpo del mensaje mediante una clave de sesión compartida por el remitente y el destinatario. El equipo MAC se anexa al mensaje que se envía al destinatario. El destinatario del mensaje vuelve a generar el MAC, usando la clave de sesión compartida y el cuerpo del mensaje, y compara el MAC generado con el MAC recibido del remitente. Si los dos son idénticos, el remitente debe tener la clave de sesión compartida y el mensaje no se ha modificado en tránsito.

En los protocolos Schannel, el algoritmo que [](cipher-suites-in-schannel.md) se usa para generar el MAC viene determinado por el conjunto de cifrado en uso por el remitente y el destinatario.

 

 
