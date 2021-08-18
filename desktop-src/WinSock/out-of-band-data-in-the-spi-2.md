---
description: Los proveedores de servicios que admiten la abstracción de datos fuera de banda (OOB) para los sockets de estilo de flujo deben cumplir la semántica de esta sección.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Datos fuera de banda en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858e2845e9fbe198dc7af7a70edfad8a4ac429f8f1abe84289b87a779f6e478b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741061"
---
# <a name="out-of-band-data-in-the-spi"></a>Datos fuera de banda en el SPI

Los proveedores de servicios que admiten la abstracción de datos fuera de banda (OOB) para los sockets de estilo de flujo deben cumplir la semántica de esta sección. Describiremos el control de datos de OOB de forma independiente del protocolo. Consulte los anexos [de Winsock](winsock-annexes.md) para obtener una explicación de los datos de OOB implementados mediante datos urgentes en proveedores de servicios TCP/IP. A continuación, el uso de [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) también se aplica a [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).

 

 
