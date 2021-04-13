---
description: El mensaje con doble cifrado consta del mensaje cifrado, los certificados de los destinatarios deseados y el conjunto de claves cifradas, uno para cada destinatario. El mensaje generado está en \# formato PKCS 7/CMS.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Crear y recibir mensajes de datos con doble cifrado en CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360229"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a>Crear y recibir mensajes de datos con doble cifrado en CAPICOM

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]

Un mensaje con doble cifrado es un mensaje cifrado para un conjunto de destinatarios. En el proceso de envoltura, se genera una clave de cifrado de sesión y se cifra el mensaje con esa clave. La propia clave de cifrado se cifra entonces por separado para cada destinatario mediante las claves públicas de cada certificado de destinatario previsto. El mensaje con doble cifrado consta del mensaje cifrado, los certificados de los destinatarios deseados y el conjunto de claves cifradas, uno para cada destinatario. El mensaje generado está en \# formato PKCS 7/CMS.

En las secciones siguientes se muestran procedimientos y ejemplos de tareas de mensajes con envoltura:

-   [Envío de un mensaje de datos con doble cifrado](sending-an-enveloped-data-message.md)
-   [Recibir un mensaje de datos con doble cifrado](receiving-an-enveloped-data-message.md)

 

 



