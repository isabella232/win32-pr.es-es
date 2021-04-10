---
description: Los proveedores de servicios que admiten la abstracción de datos fuera de banda (OOB) para los sockets de estilo de secuencia deben cumplir la semántica de esta sección.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Datos fuera de banda en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9808fa301073bcbb06be23a9487c2a1fa4f14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082113"
---
# <a name="out-of-band-data-in-the-spi"></a>Datos fuera de banda en el SPI

Los proveedores de servicios que admiten la abstracción de datos fuera de banda (OOB) para los sockets de estilo de secuencia deben cumplir la semántica de esta sección. Describiremos el control de los datos de OOB de manera independiente del protocolo. Consulte los [anexos de Winsock](winsock-annexes.md) para obtener una descripción de los datos de OOB implementados mediante datos urgentes en proveedores de servicios TCP/IP. En el siguiente, el uso de [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) también se aplica a [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).

 

 
