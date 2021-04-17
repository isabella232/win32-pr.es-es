---
description: Usar el \_ \_ código de comando de ámbito de multidifusión de SiO para especificar el ámbito en el que se debe producir la multidifusión.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: Ioctl SIO_MULTICAST_SCOPE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697486"
---
# <a name="sio_multicast_scope-ioctl"></a>SIO \_ ámbito de multidifusión \_ ioctl

Cuando se emplea la multidifusión, normalmente es necesario especificar el ámbito en el que se debe producir la multidifusión. Aquí el ámbito se define como el número de segmentos de red enrutados que se van a cubrir. El \_ \_ código de comando SiO multidifusión Scope para [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) se usa para controlar esto. Un ámbito de cero indicaría que la transmisión por multidifusión no se colocaría en la conexión, pero podría diseminarse a través de sockets dentro del host local. Un valor de ámbito de uno (valor predeterminado) indica que la transmisión se colocará en la conexión, pero no cruzará ningún enrutador. Los valores de ámbito más altos determinan el número de enrutadores que se pueden cruzar. Tenga en cuenta que esto corresponde al parámetro Time-to-Live (TTL) de la multidifusión IP.

 

 
