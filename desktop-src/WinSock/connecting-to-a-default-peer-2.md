---
description: WSPConnect establece una dirección de destino predeterminada para permitir el uso de un socket con las siguientes operaciones de envío (WSPSend) y recepción (WSPRecv).
ms.assetid: efd57cb1-9736-4527-8e20-ab9304e3a8f6
title: Conexión a un elemento del mismo nivel predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22ca4aff0cdc8560459dd2571d79a71a85fcc71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696391"
---
# <a name="connecting-to-a-default-peer"></a>Conexión a un elemento del mismo nivel predeterminado

Para un socket enlazado a un protocolo sin conexión, la operación realizada por [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) es simplemente establecer una dirección de destino predeterminada para que el socket se pueda usar con operaciones de envío y recepción orientadas a conexiones posteriores ([**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))). Se descartarán los datagramas recibidos de una dirección que no sea la dirección de destino especificada.

 

 
