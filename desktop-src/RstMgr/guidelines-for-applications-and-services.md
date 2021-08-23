---
title: Directrices para aplicaciones y servicios
description: Para reducir el número de reinicios del sistema al instalar y atender aplicaciones en Windows Vista o Windows Server 2008, debe observar las siguientes directrices para permitir que la aplicación o el servicio se apaguen y reinicien de forma limpia.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1d4aa10da60ca5019a723ec996532ac5b60fdbfcdb7c322ff07ecbf8681f37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010163"
---
# <a name="guidelines-for-applications-and-services"></a>Directrices para aplicaciones y servicios

Para reducir el número de reinicios del sistema al instalar y atender aplicaciones en Windows Vista o Windows Server 2008, debe observar las siguientes directrices para permitir que la aplicación o el servicio se apaguen y reinicien de forma limpia.

-   Las aplicaciones y los servicios deben estar preparados para que el sistema los apague y reinicie cuando sea necesario para instalar una actualización. Normalmente, cuando se instala una actualización, es necesario apagar una aplicación o un servicio porque actualmente contiene un archivo afectado en uso. Todas las aplicaciones o servicios que pueden contener un archivo en uso durante una actualización deben estar preparados para apagarse correctamente.
-   Las aplicaciones deben guardar los datos de usuario y la información de estado que se necesitan después de un reinicio y deben cumplir las directrices que se describen en la sección [Directrices para aplicaciones](guidelines-for-applications.md).
-   Los servicios deben cumplir las directrices que se describen en la sección [Directrices para servicios](guidelines-for-services.md).
-   El Administrador de reinicio no cierra los [servicios críticos del sistema](critical-system-services.md); Por lo tanto, estos servicios deben limitar el número de archivos DLL de los que dependen.

 

 




