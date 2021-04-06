---
title: Ancho de banda de red
description: Las transferencias en segundo plano solo usan ancho de banda de red inactivo en un esfuerzo por mantener la experiencia interactiva del usuario con otras aplicaciones de red, como Internet Explorer.
ms.assetid: c0b92a33-7afc-4250-8549-54cc46013239
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 39a38a0efd5f2caea432fc9d13f7a958b6bcd407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077987"
---
# <a name="network-bandwidth"></a>Ancho de banda de red

Las transferencias en segundo plano solo usan ancho de banda de red inactivo en un esfuerzo por mantener la experiencia interactiva del usuario con otras aplicaciones de red, como los exploradores Web. BITS ajusta el uso del ancho de banda a medida que el usuario aumenta o disminuye el uso del ancho de banda. Tenga en cuenta que BITS sigue transfiere una pequeña cantidad de datos durante el uso intensivo de la red para asegurarse de que los trabajos de BITS progresan.

BITS supervisa el tráfico de red en el dispositivo de puerta de enlace a Internet (IGD) o la tarjeta de interfaz de red (NIC) del cliente y usa solo la parte inactiva del ancho de banda de red. BITS también habilita [LEDBAT](https://blogs.technet.microsoft.com/networking/2018/07/25/ledbat/) en conexiones http para ayudar a aliviar la congestión de la red.

Si BITS usa la tarjeta de interfaz de red para medir el tráfico y no hay aplicaciones de red que se ejecuten en el cliente, BITS consumirá la mayor parte del ancho de banda disponible. Esto no significa que la red más allá del cliente esté inactiva; la red puede tener una capacidad completa.

Esto puede ser un problema si el cliente tiene un adaptador de red rápido pero la conexión completa a Internet se realiza a través de un vínculo de baja velocidad (por ejemplo, un enrutador DSL), ya que BITS compite por el ancho de banda completo en lugar de usar solo el ancho de banda disponible en el vínculo de baja velocidad; BITS no tiene visibilidad del tráfico de red más allá del cliente.

Un dispositivo de puerta de enlace que admita contadores puede eliminar este problema porque BITS mediría el tráfico en el vínculo lento y usaría el ancho de banda adecuado. Si el dispositivo no admite los contadores, puede reducir el impacto de este tipo de conexión mediante el uso de la directiva **MaxInternetBandwidth** para limitar el ancho de banda que usa bits en el equipo cliente. Para obtener más información, consulte [directivas de grupo](group-policies.md).

Si el equipo contiene varias interfaces de red, como un módem, una red privada virtual (VPN) y varias tarjetas de interfaz de red (NIC), BITS llama a la función auxiliar de IP, [**GetBestInterfaceEx**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterfaceex), para determinar la interfaz que tiene la mejor ruta a la dirección IP especificada. BITS supervisará el uso de ancho de banda en esa interfaz.

## <a name="using-an-internet-gateway-device-igd-to-determine-usage"></a>Uso de un dispositivo de puerta de enlace a Internet (IGD) para determinar el uso

Para usar un dispositivo de puerta de enlace, el dispositivo debe ser compatible con los contadores de bytes (el dispositivo debe responder a las acciones GetTotalBytesSent y GetTotalBytesReceived) y el Plug and Play universal (UPnP) debe estar habilitado.

BITS usará la tarjeta de interfaz de red si:

-   El dispositivo de puerta de enlace no admite los contadores
-   UPnP no está habilitado
-   El servidor está en la misma subred
-   El dispositivo de puerta de enlace no devuelve los datos del contador en menos de 200 TICs

Si el usuario usa un perfil de red pública, el perfil debe permitir UPnP. De forma predeterminada, los perfiles de red privada y de dominio permiten UPnP.

Si se usa una conexión VPN, BITS usa el primer dispositivo que UPnP devuelve.