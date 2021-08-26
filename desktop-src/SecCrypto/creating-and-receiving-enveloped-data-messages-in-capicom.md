---
description: El mensaje sobre consiste en el mensaje cifrado, los certificados de los destinatarios previstos y el conjunto de claves cifradas, uno para cada destinatario. El mensaje generado está en formato PKCS \# 7/CMS.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Creación y recepción de mensajes de datos sobres en CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4024516333b7dd416f788f181f2ac36e5e0f4e015953cdab26d08b48da16c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876546"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a>Creación y recepción de mensajes de datos sobres en CAPICOM

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

Un mensaje sobre es un mensaje cifrado para un conjunto de destinatarios. En el proceso de envolver, se genera una clave de cifrado de sesión y el mensaje se cifra con esa clave. A continuación, la propia clave de cifrado se cifra por separado para cada destinatario mediante las claves públicas del certificado de cada destinatario previsto. El mensaje sobre consiste en el mensaje cifrado, los certificados de los destinatarios previstos y el conjunto de claves cifradas, uno para cada destinatario. El mensaje generado está en formato PKCS \# 7/CMS.

En las secciones siguientes se muestran procedimientos y ejemplos para las tareas de mensaje envoltorio:

-   [Envío de un mensaje de datos sobres](sending-an-enveloped-data-message.md)
-   [Recepción de un mensaje de datos sobres](receiving-an-enveloped-data-message.md)

 

 



