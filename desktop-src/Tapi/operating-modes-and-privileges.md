---
description: La aplicación puede solicitar uno de los dos modos de funcionamiento al abrir un dispositivo telefónico.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Modos de funcionamiento y privilegios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba1cc01ed0552762ac3bc97449b1ae5a923cb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812488"
---
# <a name="operating-modes-and-privileges"></a>Modos de funcionamiento y privilegios

La aplicación puede solicitar uno de los dos modos de funcionamiento al abrir un dispositivo telefónico. Estos modos reflejan los privilegios que la aplicación solicita para el dispositivo:

-   La apertura de un teléfono para los privilegios de monitor permite a la aplicación determinar el estado del dispositivo de teléfono. Los mensajes se envían a la aplicación cuando se detectan cambios de estado en el dispositivo telefónico.
-   Una aplicación que abre un dispositivo telefónico para privilegios de propietario puede usar operaciones que modifican el estado del dispositivo de teléfono. El privilegio Owner también incluye automáticamente los privilegios de supervisión completos. En cualquier momento, un dispositivo telefónico determinado solo se puede abrir una vez para los privilegios de propietario, pero varias veces para los privilegios de supervisión. Todas las operaciones de **phoneSet** requieren privilegios de propietario, mientras que todas las operaciones de **phoneGet** solo requieren privilegios de monitor.

 

 



