---
description: Uso del código de \_ comando SIO MULTICAST \_ SCOPE para especificar el ámbito en el que se debe producir la multidifusión.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE Ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be65ee600b680805177a44125c03e65e49364ae9008d306349da8f60f9d9de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559693"
---
# <a name="sio_multicast_scope-ioctl"></a>IOCTL \_ DE ÁMBITO DE \_ MULTIDIFUSIÓN DE SIO

Cuando se emplea la multidifusión, normalmente es necesario especificar el ámbito en el que se debe producir la multidifusión. Aquí se define el ámbito para que sea el número de segmentos de red enrutados que se va a cubrir. El código de comando \_ SIO MULTICAST \_ SCOPE para [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) se usa para controlar esto. Un ámbito de cero indicaría que la transmisión de multidifusión no se colocaría en la conexión, pero se podría propagar entre sockets dentro del host local. Un valor de ámbito de uno (el valor predeterminado) indica que la transmisión se colocará en la conexión, pero no cruzará ningún enrutador. Los valores de ámbito más altos determinan el número de enrutadores que se pueden cruzar. Tenga en cuenta que esto corresponde al parámetro de período de vida (TTL) en la multidifusión IP.

 

 
