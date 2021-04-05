---
description: Cuando se emplea la multidifusión, normalmente es necesario especificar el ámbito en el que se debe producir la multidifusión.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: Código de comando de SIO_MULTICAST_SCOPE para WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a43e461907dcded8e59c6ffee9b1376989d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082399"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a>\_ \_ Código de comando de ámbito de multidifusión de SiO para WSAIoctl

Cuando se emplea la multidifusión, normalmente es necesario especificar el *ámbito* en el que se debe producir la multidifusión. El ámbito se define como el número de segmentos de red enrutados que se van a cubrir. Un ámbito de cero indicaría que la transmisión por multidifusión no se colocaría en la conexión, pero podría diseminarse a través de sockets dentro del host local. Un valor de ámbito de 1 (valor predeterminado) indica que la transmisión se colocará en la conexión, pero no cruzará ningún enrutador. Los valores de ámbito más altos determinan el número de enrutadores que se pueden cruzar. Tenga en cuenta que esto corresponde al parámetro Time-to-Live (TTL) de la multidifusión IP.

La función [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) se usa para unir un nodo hoja a la sesión multipoint. Vea lo siguiente para obtener una explicación sobre cómo se emplea esta función.

 

 



