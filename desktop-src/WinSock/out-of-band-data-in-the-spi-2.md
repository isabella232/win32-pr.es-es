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
# <a name="out-of-band-data-in-the-spi"></a><span data-ttu-id="19c08-103">Datos fuera de banda en el SPI</span><span class="sxs-lookup"><span data-stu-id="19c08-103">Out-of-Band Data in the SPI</span></span>

<span data-ttu-id="19c08-104">Los proveedores de servicios que admiten la abstracción de datos fuera de banda (OOB) para los sockets de estilo de secuencia deben cumplir la semántica de esta sección.</span><span class="sxs-lookup"><span data-stu-id="19c08-104">The service providers which support the out-of-band data (OOB) abstraction for the stream-style sockets must adhere to the semantics in this section.</span></span> <span data-ttu-id="19c08-105">Describiremos el control de los datos de OOB de manera independiente del protocolo.</span><span class="sxs-lookup"><span data-stu-id="19c08-105">We will describe OOB data handling in a protocol-independent manner.</span></span> <span data-ttu-id="19c08-106">Consulte los [anexos de Winsock](winsock-annexes.md) para obtener una descripción de los datos de OOB implementados mediante datos urgentes en proveedores de servicios TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="19c08-106">Please refer to the [Winsock Annexes](winsock-annexes.md) for a discussion of OOB data implemented using urgent data in TCP/IP service providers.</span></span> <span data-ttu-id="19c08-107">En el siguiente, el uso de [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) también se aplica a [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="19c08-107">In the following, the use of [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) also applies to [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span></span>

 

 
