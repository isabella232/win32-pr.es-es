---
description: Muestra el uso de funciones de red hospedada inalámbricas.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Ejemplo de red hospedada inalámbrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473725"
---
# <a name="wireless-hosted-network-sample"></a>Ejemplo de red hospedada inalámbrica

Un ejemplo de red hospedada inalámbrica que muestra el uso de funciones de red hospedada inalámbricas se incluye con el Kit de desarrollo de software (SDK) de Microsoft Windows. La versión más reciente del SDK Windows está disponible en el [Centro de descarga](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)de .

De forma predeterminada, el código fuente de ejemplo de red hospedada inalámbrica se instala en el directorio siguiente:

**C: \\ Archivos de programa Sdk de Microsoft Windows \\ \\ \\ v7.0 \\ Samples \\ NetDs \\ Wlan**

El ejemplo de red hospedada inalámbrica se encuentra en la carpeta siguiente:

**WirelessHostedNetwork**

El ejemplo de red hospedada inalámbrica se puede compilar en el SDK Windows para Windows 7. El ejemplo de red hospedada inalámbrica se puede ejecutar en Windows 7 y en Windows Server 2008 R2 con el servicio LAN inalámbrico instalado.

En Windows 7 y en Windows Server 2008 R2 con el servicio laN inalámbrica instalado, el sistema operativo instala un dispositivo virtual si hay un adaptador inalámbrico compatible con la red hospedada en la máquina. Este dispositivo virtual normalmente se muestra en la "Carpeta de conexiones de red" como "Conexión de red inalámbrica 2" con un nombre de dispositivo de "Adaptador de minipuerto De Wi-Fi virtual de Microsoft" si el equipo tiene un único adaptador de red inalámbrica. Este dispositivo virtual se usa exclusivamente para realizar conexiones de punto de acceso de software (SoftAP). La duración de este dispositivo virtual está vinculada al adaptador inalámbrico físico. Si el adaptador inalámbrico físico está deshabilitado, este dispositivo virtual también se quitará.

Las funciones de red hospedada inalámbrica se usan para iniciar y detener la red hospedada inalámbrica, configurar o cambiar la configuración o consultar información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la red hospedada inalámbrica](about-the-wireless-hosted-network.md)
</dt> <dt>

[Uso del uso compartido de redes hospedadas e Internet](using-hosted-network-and-internet-connection-sharing.md)
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

 

 



