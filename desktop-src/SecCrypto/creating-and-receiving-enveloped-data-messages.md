---
description: Un mensaje con doble cifrado es un mensaje cifrado para un destinatario o un conjunto de destinatarios.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Crear y recibir mensajes de datos con doble cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d973ded4656966d1b61ac0ae9779acf35eb578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666422"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a>Crear y recibir mensajes de datos con doble cifrado

Un mensaje con doble cifrado es un mensaje cifrado para un conjunto de destinatarios. En el proceso de envoltura, se genera una clave de cifrado de sesión y se cifra el mensaje con esa clave. La propia clave de cifrado se cifra entonces por separado para cada destinatario mediante las claves públicas de cada certificado de destinatario previsto. El mensaje con doble cifrado consta del mensaje cifrado, los certificados de los destinatarios deseados y el conjunto de claves cifradas, uno para cada destinatario. El mensaje generado está en formato [*PKCS \# 7*](../secgloss/p-gly.md)/CMS.

En las secciones siguientes se muestran procedimientos y ejemplos de tareas de mensajes con envoltura:

-   [Codificación de datos con doble cifrado](encoding-enveloped-data.md)
-   [Descodificar datos con doble cifrado](decoding-enveloped-data.md)
-   [Código alternativo para codificar un mensaje con doble cifrado](alternate-code-for-encoding-an-enveloped-message.md)
-   [Programa C de ejemplo: codificar un mensaje con signo de cifrado](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
