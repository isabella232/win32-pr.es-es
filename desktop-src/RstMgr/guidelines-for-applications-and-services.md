---
title: Directrices para aplicaciones y servicios
description: Para reducir el número de reinicios del sistema al instalar y dar servicio a las aplicaciones en Windows Vista o Windows Server 2008, debe seguir estas directrices para permitir que la aplicación o el servicio se cierren correctamente y se reinicien.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651292"
---
# <a name="guidelines-for-applications-and-services"></a>Directrices para aplicaciones y servicios

Para reducir el número de reinicios del sistema al instalar y dar servicio a las aplicaciones en Windows Vista o Windows Server 2008, debe seguir estas directrices para permitir que la aplicación o el servicio se cierren correctamente y se reinicien.

-   Las aplicaciones y los servicios deben estar preparados para que el sistema los cierre y lo reinicie cuando sea necesario para instalar una actualización. Normalmente, cuando se instala una actualización, una aplicación o servicio debe cerrarse porque actualmente contiene un archivo afectado en uso. Todas las aplicaciones o servicios que pueden contener un archivo en uso durante una actualización deben estar preparados para cerrarse sin problemas.
-   Las aplicaciones deben guardar los datos de usuario y la información de estado que se necesitan después de un reinicio y deben cumplir las directrices descritas en la sección [directrices para aplicaciones](guidelines-for-applications.md).
-   Los servicios deben cumplir las directrices descritas en la sección [directrices para servicios](guidelines-for-services.md).
-   El administrador de reinicio no cierra los [servicios críticos del sistema](critical-system-services.md); por lo tanto, estos servicios deben limitar el número de archivos dll de los que dependen.

 

 




