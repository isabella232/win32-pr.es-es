---
description: Se usa un código de autenticación de mensajes (MAC) para detectar la manipulación y falsificación de mensajes.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Códigos de autenticación de mensajes en Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173486"
---
# <a name="message-authentication-codes-in-schannel"></a>Códigos de autenticación de mensajes en Schannel

Se [*usa un código de*](../secgloss/m-gly.md) autenticación de mensajes (MAC) para detectar la manipulación y falsificación de mensajes. El remitente de un mensaje crea un MAC mediante el cifrado [](../secgloss/s-gly.md) de un [*hash*](../secgloss/h-gly.md) unitorio del cuerpo del mensaje mediante una clave de sesión compartida por el remitente y el destinatario. El MAC se anexa al mensaje que se envía al destinatario. El destinatario del mensaje genera el MAC de nuevo, usando la clave de sesión compartida y el cuerpo del mensaje, y compara el MAC generado con el MAC recibido del remitente. Si los dos son idénticos, el remitente debe tener la clave de sesión compartida y el mensaje no se ha modificado en tránsito.

En los protocolos Schannel, el algoritmo que [](cipher-suites-in-schannel.md) se usa para generar el MAC viene determinado por el conjunto de cifrado en uso por el remitente y el destinatario.

 

 
