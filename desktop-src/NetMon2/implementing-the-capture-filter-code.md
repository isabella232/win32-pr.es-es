---
description: Después de determinar cómo organizar el filtro a través de una estructura CAPTUREFILTER, debe asignar y rellenar la estructura, que se pasa a la Monitor de red controlador a través de un BLOB de configuración.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Implementar el código de filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913858"
---
# <a name="implementing-the-capture-filter-code"></a>Implementar el código de filtro de captura

Después de determinar cómo organizar el filtro a través de una estructura [**CAPTUREFILTER**](capturefilter.md) , debe asignar y rellenar la estructura, que se pasa a la monitor de red controlador a través de un BLOB de configuración.

Los usuarios directos de NPP agregan el filtro de captura al BLOB de configuración que se pasa a **Connect**, [**Configure**](configure.md)o ambos. Para obtener una lista de las interfaces COM que puede usar para comunicarse con el NPP, consulte [interfaces NPP](npp-interfaces.md).

 

 



