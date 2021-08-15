---
description: Cuando se emplea la multidifusión, normalmente es necesario especificar el ámbito en el que debe producirse la multidifusión.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE de comandos para WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38269167aa2ed142440b0e1105600d26c59514f72d749595ce44ecdf3a0998f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927374"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a>Código de comando DE ÁMBITO DE MULTIDIFUSIÓN DE SIO \_ para \_ WSAIoctl

Cuando se emplea la multidifusión, normalmente es necesario especificar el *ámbito en* el que debe producirse la multidifusión. El ámbito se define como el número de segmentos de red enrutados que se va a cubrir. Un ámbito de cero indicaría que la transmisión de multidifusión no se colocaría en la conexión, pero se podría distribuir entre sockets dentro del host local. Un valor de ámbito de 1 (valor predeterminado) indica que la transmisión se colocará en la conexión, pero no atravesará ningún enrutador. Los valores de ámbito más altos determinan el número de enrutadores que se pueden atravesar. Tenga en cuenta que esto corresponde al parámetro de período de vida (TTL) en la multidifusión IP.

La función [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) se usa para unir un nodo hoja a la sesión de varios puntos. Consulte lo siguiente para obtener una explicación sobre cómo se utiliza esta función.

 

 



