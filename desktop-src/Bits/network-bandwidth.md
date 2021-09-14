---
title: Ancho de banda de red
description: Las transferencias en segundo plano solo usan ancho de banda de red inactivo en un esfuerzo por conservar la experiencia interactiva del usuario con otras aplicaciones de red, como Internet Explorer.
ms.assetid: c0b92a33-7afc-4250-8549-54cc46013239
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 39a38a0efd5f2caea432fc9d13f7a958b6bcd407
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974637"
---
# <a name="network-bandwidth"></a>Ancho de banda de red

Las transferencias en segundo plano solo usan ancho de banda de red inactivo en un esfuerzo por conservar la experiencia interactiva del usuario con otras aplicaciones de red, como los exploradores web. BITS ajusta su uso del ancho de banda a medida que el usuario aumenta o disminuye su uso del ancho de banda. Tenga en cuenta que BITS todavía transfiere una pequeña cantidad de datos durante el uso elevado de la red para asegurarse de que los trabajos de BITS progresan.

BITS supervisa el tráfico de red en el dispositivo de puerta de enlace de Internet (IGD) o en la tarjeta de interfaz de red (NIC) del cliente y usa solo la parte inactiva del ancho de banda de red. BITS también habilita [LEDBAT en](https://blogs.technet.microsoft.com/networking/2018/07/25/ledbat/) conexiones HTTP para ayudar a mitigar la congestión de la red.

Si BITS usa la tarjeta de interfaz de red para medir el tráfico y no hay aplicaciones de red que se ejecuten en el cliente, BITS consumirá la mayor parte del ancho de banda disponible. Esto no significa que la red más allá del cliente esté inactiva; la red podría estar a plena capacidad.

Esto puede ser un problema si el cliente tiene un adaptador de red rápido, pero la conexión a Internet completa es a través de un vínculo lento (como un enrutador DSL) porque BITS competirá por el ancho de banda completo en lugar de usar solo el ancho de banda disponible en el vínculo lento. BITS no tiene visibilidad del tráfico de red más allá del cliente.

Un dispositivo de puerta de enlace que admita contadores puede eliminar este problema porque BITS mediría el tráfico en el vínculo lento y usaría el ancho de banda adecuadamente. Si el dispositivo no admite contadores, puede reducir el impacto de este tipo de conexión mediante la directiva **MaxInternetBandwidth** para limitar el ancho de banda que bits usa en el equipo cliente. Para más información, consulte [Directivas de grupo.](group-policies.md)

Si el equipo contiene varias interfaces de red, como un módem, una red privada virtual (VPN) y varias tarjetas de interfaz de red (NIC), BITS llama a la función del asistente de IP, [**GetBestInterfaceEx**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterfaceex), para determinar la interfaz que tiene la mejor ruta a la dirección IP especificada. Bits supervisará entonces el uso del ancho de banda en esa interfaz.

## <a name="using-an-internet-gateway-device-igd-to-determine-usage"></a>Uso de un dispositivo de puerta de enlace de Internet (IGD) para determinar el uso

Para usar un dispositivo de puerta de enlace, el dispositivo debe admitir contadores de bytes (el dispositivo debe responder a las acciones GetTotalBytesSent y GetTotalBytesReceived) y el Plug and Play universal (UPnP) debe estar habilitado.

BITS usará la tarjeta de interfaz de red si:

-   El dispositivo de puerta de enlace no admite los contadores
-   UPnP no está habilitado
-   El servidor está dentro de la misma subred.
-   El dispositivo de puerta de enlace no devuelve los datos del contador en menos de 200 tics

Si el usuario usa un perfil de red pública, el perfil debe permitir UPnP. De forma predeterminada, los perfiles de red privada y de dominio permiten UPnP.

Si se usa una conexión VPN, BITS usa el primer dispositivo que devuelve UPnP.