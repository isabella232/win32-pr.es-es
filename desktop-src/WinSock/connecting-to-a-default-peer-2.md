---
description: WSPConnect establece una dirección de destino predeterminada para permitir que se utilice un socket con operaciones de envío y recepción (WSPRecv) posteriores.
ms.assetid: efd57cb1-9736-4527-8e20-ab9304e3a8f6
title: Conexión a un punto de conexión predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00da810046f8b7f583807eea5dd6a577fbd46fc32ff4abcce7d095c8a05ed68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112413"
---
# <a name="connecting-to-a-default-peer"></a>Conexión a un punto de conexión predeterminado

En el caso de un socket enlazado a un protocolo sin conexión, la operación realizada por [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) es simplemente establecer una dirección de destino predeterminada para que el socket se pueda usar con las posteriores operaciones de envío y recepción orientadas a la conexión [**(WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPRecv).**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) Se descartarán todos los datagramas recibidos de una dirección que no sea la dirección de destino especificada.

 

 
