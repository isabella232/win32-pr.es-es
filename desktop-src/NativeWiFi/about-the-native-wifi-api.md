---
description: Native Wifi API contiene funciones, estructuras y enumeraciones que admiten la conectividad de red inalámbrica y la administración de perfiles inalámbricos.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Acerca de la API de Wi-Fi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473748"
---
# <a name="about-the-native-wifi-api"></a>Acerca de la API de Wi-Fi nativa

Native Wifi API contiene funciones, estructuras y enumeraciones que admiten la conectividad de red inalámbrica y la administración de perfiles inalámbricos. La API se puede usar para redes ad hoc y de infraestructura. La API ad hoc inalámbrica es una interfaz simplificada orientada a objetos para crear, administrar y usar redes ad hoc.

> [!Note]  
> Es posible que el modo ad hoc no esté disponible en versiones futuras de Windows. A partir de Windows 8.1 y Windows Server 2012 R2, use Wi-Fi Direct en [su lugar.](about-the-wi-fi-direct-api.md)

 

La implementación de la API ad hoc usa la API Wifi nativa. Esto significa que las llamadas API ad hoc pueden desencadenar notificaciones wi-fi nativas y viceversa.

No se recomienda combinar llamadas API Wi-Fi nativas y llamadas API ad hoc inalámbricas. Los desarrolladores deben elegir un enfoque de programación antes de diseñar una aplicación. Si la aplicación usa o administra redes de infraestructura, debe usar native Wifi API. Si la aplicación requiere la funcionalidad de administración de perfiles, debe usar native Wifi API. De lo contrario, debe usar la API ad hoc inalámbrica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Wi-Fi nativo](about-native-wifi.md)
</dt> <dt>

[Compatibilidad nativa de la API wifi en Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[Permisos nativos de la API wifi](native-wifi-api-permissions.md)
</dt> <dt>

[Acerca de la API ad hoc inalámbrica](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Descarga del SDK Windows Vista](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



