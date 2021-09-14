---
description: Para establecer una conexión entre un cliente y un servidor mediante el protocolo SMB de Microsoft, primero debe determinar el dialecto con el nivel más alto de funcionalidad que admiten el cliente y el servidor.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Dialectos de protocolo SMB de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069909"
---
# <a name="microsoft-smb-protocol-dialects"></a>Dialectos de protocolo SMB de Microsoft

La lista de paquetes de mensajes del Protocolo SMB de Microsoft ha aumentado a lo largo de los años para dar cabida a la funcionalidad creciente del protocolo SMB de Microsoft y ahora se cifra en cientos. Cada fase de su crecimiento está marcada por un conjunto de paquetes estándar, o dialecto. Cada dialecto se identifica mediante una cadena estándar como "PC NETWORK PROGRAM 1.0", "MICROSOFT NETWORKS 3.0", "DOS LANMAN 2.1" o "NT LM 0.12". La primera cadena identifica el primer dialecto de SMB y la última cadena identifica CIFS, el primer dialecto del protocolo SMB de Microsoft.

La mayoría de los clientes de Windows admiten al menos seis dialectos diferentes del protocolo SMB de Microsoft, por lo que uno de los primeros pasos para establecer una conexión entre un cliente y un servidor mediante el Protocolo SMB de Microsoft es determinar el dialecto con el nivel más alto de funcionalidad que admiten el cliente y el servidor. Este proceso se conoce como "negociación del dialecto". Las cadenas de dialecto mencionadas anteriormente se incluyen en los paquetes de solicitud y respuesta de negociación de dialectos para este propósito.

 

 



