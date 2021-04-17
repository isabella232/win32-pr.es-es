---
description: Muestra el uso de las funciones de red hospedada inalámbrica.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Ejemplo de red hospedada inalámbrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677415"
---
# <a name="wireless-hosted-network-sample"></a>Ejemplo de red hospedada inalámbrica

En el kit de desarrollo de software (SDK) de Microsoft Windows se incluye un ejemplo de red hospedada inalámbrica que muestra el uso de las funciones de red hospedada inalámbrica. La versión más reciente del Windows SDK está disponible en el [centro de descarga](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).

De forma predeterminada, el código fuente de ejemplo de red hospedada inalámbrica se instala en el directorio siguiente:

**C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ NetDs \\ WLAN**

El ejemplo de red hospedada inalámbrica se encuentra en la siguiente carpeta:

**WirelessHostedNetwork**

El ejemplo de red hospedada inalámbrica se puede compilar en el Windows SDK para Windows 7. El ejemplo de red hospedada inalámbrica se puede ejecutar en Windows 7 y en Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado.

En Windows 7 y en Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado, el sistema operativo instala un dispositivo virtual si hay un adaptador inalámbrico compatible con redes hospedadas en la máquina. Este dispositivo virtual normalmente se muestra en la "carpeta conexiones de red" como "conexión de red inalámbrica 2" con el nombre de dispositivo "adaptador de minipuerto de Microsoft Virtual WiFi" si el equipo tiene un único adaptador de red inalámbrica. Este dispositivo virtual se utiliza exclusivamente para realizar conexiones de punto de acceso de software (SoftAP). La duración de este dispositivo virtual está ligada al adaptador inalámbrico físico. Si el adaptador inalámbrico físico está deshabilitado, este dispositivo virtual también se quitará.

Las funciones de red hospedada inalámbrica se usan para iniciar y detener la red hospedada inalámbrica, configurar o cambiar la configuración o consultar información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la red hospedada inalámbrica](about-the-wireless-hosted-network.md)
</dt> <dt>

[Uso de redes hospedadas y conexión compartida a Internet](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



