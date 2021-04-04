---
description: Un código de autentificación de mensajes (MAC) (MAC) se usa para detectar la alteración y falsificación de mensajes.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Códigos de autenticación de mensajes en Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278130"
---
# <a name="message-authentication-codes-in-schannel"></a>Códigos de autenticación de mensajes en Schannel

Un [*código de autentificación de mensajes (Mac)*](../secgloss/m-gly.md) (Mac) se usa para detectar la alteración y falsificación de mensajes. El remitente de un mensaje crea un equipo MAC mediante el cifrado de un [*hash*](../secgloss/h-gly.md) unidireccional del cuerpo del mensaje mediante una [*clave de sesión*](../secgloss/s-gly.md) compartida por el remitente y el destinatario. El equipo MAC se anexa al mensaje que se envía al destinatario. El destinatario del mensaje vuelve a generar el equipo MAC, con la clave de sesión compartida y el cuerpo del mensaje, y compara el equipo MAC generado con el equipo MAC recibido del remitente. Si los dos son idénticos, el remitente debe tener la clave de sesión compartida y el mensaje no se ha modificado en tránsito.

En los protocolos Schannel, el algoritmo utilizado para generar el equipo MAC viene determinado por el [conjunto de cifrado](cipher-suites-in-schannel.md) que usa el remitente y el destinatario.

 

 
