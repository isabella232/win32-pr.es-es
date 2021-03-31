---
description: La API WiFi nativa contiene funciones, estructuras y enumeraciones que admiten la conectividad de red inalámbrica y la administración de perfiles inalámbricos.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Acerca de la API nativa WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279004"
---
# <a name="about-the-native-wifi-api"></a>Acerca de la API nativa WiFi

La API WiFi nativa contiene funciones, estructuras y enumeraciones que admiten la conectividad de red inalámbrica y la administración de perfiles inalámbricos. La API se puede usar para las redes de infraestructura y ad hoc. La API ad hoc inalámbrica es una interfaz simplificada orientada a objetos para crear, administrar y usar redes ad hoc.

> [!Note]  
> El modo ad hoc podría no estar disponible en versiones futuras de Windows. A partir de Windows 8.1 y Windows Server 2012 R2, utilice en su lugar [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .

 

La implementación de la API ad hoc usa la API WiFi nativa. Esto significa que las llamadas de la API ad hoc pueden desencadenar notificaciones WiFi nativas y viceversa.

No se recomienda mezclar llamadas nativas de la API WiFi y llamadas inalámbricas de la API ad hoc. Los desarrolladores deben elegir un enfoque de programación antes de diseñar una aplicación. Si su aplicación usa o administra redes de infraestructura, debe usar la API WiFi nativa. Si su aplicación requiere la funcionalidad de administración de perfiles, debe usar la API WiFi nativa. De lo contrario, debe usar la API ad hoc inalámbrica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WiFi nativo](about-native-wifi.md)
</dt> <dt>

[Compatibilidad con la API WiFi nativa en Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[Permisos de la API WiFi nativa](native-wifi-api-permissions.md)
</dt> <dt>

[Acerca de la API ad hoc inalámbrica](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Descargar el SDK de Windows Vista](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



