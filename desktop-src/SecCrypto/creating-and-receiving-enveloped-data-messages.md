---
description: Un mensaje con sobre es un mensaje cifrado para un destinatario o un conjunto de destinatarios.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Creación y recepción de mensajes de datos con sobres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63abf31d582ae9ae184dc15d85d827a3741d317e3bad75c8b07cce25e457bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768910"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a>Creación y recepción de mensajes de datos con sobres

Un mensaje con sobre es un mensaje cifrado para un conjunto de destinatarios. En el proceso de envolver, se genera una clave de cifrado de sesión y el mensaje se cifra con esa clave. A continuación, la propia clave de cifrado se cifra por separado para cada destinatario mediante las claves públicas del certificado de cada destinatario previsto. El mensaje con sobres consta del mensaje cifrado, los certificados de los destinatarios previstos y el conjunto de claves cifradas, uno para cada destinatario. El mensaje generado está en [*formato PKCS \# 7*](../secgloss/p-gly.md)/CMS.

En las secciones siguientes se muestran procedimientos y ejemplos para las tareas de mensaje envolvido:

-   [Codificación de datos con sobres](encoding-enveloped-data.md)
-   [Decoding Enveloped Data](decoding-enveloped-data.md)
-   [Código alternativo para codificar un mensaje con sobres](alternate-code-for-encoding-an-enveloped-message.md)
-   [Programa C de ejemplo: codificación de un mensaje con sobres con firma](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
