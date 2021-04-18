---
description: El conjunto de protocolos de Internet es el protocolo de red dominante que se utiliza en redes empresariales y en Internet.
ms.assetid: 8c123e09-b11a-4c92-b41e-49cc01be53d3
title: Compatibilidad del Protocolo de red Winsock en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36da53101dda06426a04e5f910b4548273e8ab47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497447"
---
# <a name="winsock-network-protocol-support-in-windows"></a>Compatibilidad del Protocolo de red Winsock en Windows

El conjunto de protocolos de Internet es el protocolo de red dominante que se utiliza en redes empresariales y en Internet. El conjunto de protocolos de Internet representa una gran colección de protocolos de red en capas. A menudo, el conjunto de protocolos de Internet se conoce como TCP/IP basado en dos de los protocolos más importantes incluidos en el conjunto: el protocolo de Internet (IP) y el protocolo de control de transmisión (TCP).

IPv6 e IPv4 representan las dos versiones disponibles del Protocolo de Internet. TCP es uno de los diversos servicios de red importantes a los que se suele hacer referencia como protocolos IP que funcionan a través de redes IPv6 e IPv4. El protocolo de datagramas de usuario (UDP) y el protocolo de mensajes de control de Internet (ICMP) son otros protocolos IP importantes que se usan en redes IPv6 e IPv4. Hay una serie de protocolos IP que se pueden usar en redes IPv6 e IPv4.

Windows Sockets considera que cada conjunto de protocolos de red es una familia de direcciones únicas. Por tanto, el protocolo IPv6 se considera la familia de direcciones **AF \_ inet6** y el protocolo IPv4 se considera la familia de direcciones de **AF \_ inet** . Los protocolos IPv6 e IPv4 admiten el uso de varios protocolos IP superpuestos, como TCP, UDP e ICMP.

Windows Sockets se diseñó inicialmente para agregar compatibilidad con IPv4 a Windows. Sin embargo, la interfaz de programación de Windows Sockets se diseñó desde el principio con la posibilidad de admitir otros conjuntos de protocolos de red. Con el tiempo, las versiones de Windows y los sockets de Windows asociados han incluido compatibilidad nativa con otros conjuntos de protocolos de red (por ejemplo, IPX/SPX y AppleTalk). También se ha disponible compatibilidad con otros protocolos de red para las versiones de Windows como software de terceros de los proveedores.

Antes del crecimiento y la popularidad de Internet, se usaron otros conjuntos de protocolos de red en entornos en red, especialmente en las intranets locales. La elección de un conjunto de protocolos de red solía basarse en el tamaño de la red o en la experiencia del personal de redes de ti. Con la conectividad a Internet global de hoy en día, incluso las redes más pequeñas al resto del mundo, la experiencia de red en IPv6 e IPv4 es esencial para los profesionales de redes. Como resultado, otros conjuntos de protocolos de red anteriormente importantes ahora tienen un uso muy limitado y se han vuelto obvias. La compatibilidad nativa con estos conjuntos de protocolos de red obviados, a menudo denominados protocolos de red heredados, se ha quitado de las versiones recientes de Microsoft Windows. La compatibilidad con algunos de estos protocolos heredados puede estar disponible como software de terceros de los proveedores (ATM con hardware de red ATM, por ejemplo).

En la tabla siguiente se identifica la compatibilidad nativa con Windows para conjuntos de protocolos de red comunes. 

| Protocolo de red                 | Windows 7                | Windows Server 2008      | Windows Vista            | Windows Server 2003                  | Windows XP                           | Windows 2000                         |
|----------------------------------|--------------------------|--------------------------|--------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
| IPv6<br/>                  | Compatible<br/>     | Compatible<br/>     | Compatible<br/>     | Compatible<br/>                 | Compatible<br/>                 | No compatible (vea las notas)<br/> |
| IPv4<br/>                  | Compatible<br/>     | Compatible<br/>     | Compatible<br/>     | Compatible<br/>                 | Compatible<br/>                 | Compatible<br/>                 |
| NetBIOS (vea las notas) <br/>  | Compatible<br/>     | Compatible<br/>     | Compatible<br/>     | Compatible<br/>                 | Compatible<br/>                 | Compatible<br/>                 |
| IrDA (vea las notas)<br/>      | Compatible<br/>     | Compatible<br/>     | Compatible<br/>     | Compatible<br/>                 | Compatible<br/>                 | Compatible<br/>                 |
| Bluetooth (vea las notas)<br/> | Compatible<br/>     | Compatible<br/>     | Compatible<br/>     | Compatible<br/>                 | Compatible<br/>                 | No compatible<br/>             |
| IPX/SPX<br/>               | No compatible<br/> | No compatible<br/> | No compatible<br/> | Compatible<br/>                 | Compatible<br/>                 | Compatible<br/>                 |
| AppleTalk<br/>             | No compatible<br/> | No compatible<br/> | No compatible<br/> | Compatible<br/>                 | Compatible<br/>                 | Compatible<br/>                 |
| DLC<br/>                   | No compatible<br/> | No compatible<br/> | No compatible<br/> | No compatible (vea las notas)<br/> | No compatible (vea las notas)<br/> | Compatible<br/>                 |
| Cajero automático<br/>                   | No compatible<br/> | No compatible<br/> | No compatible<br/> | Compatible (vea las notas)<br/>     | Compatible (vea las notas)<br/>     | Compatible (vea las notas)<br/>     |
| Tráfico<br/>               | No compatible<br/> | No compatible<br/> | No compatible<br/> | No compatible<br/>             | No compatible<br/>             | Compatible (vea las notas)<br/>     |



 

**IPv6 en Windows 2000:** El protocolo IPv6 es compatible con Windows 2000 con Service Pack 1 (SP1) y versiones posteriores con Microsoft IPv6 Technology Preview para Windows 2000.

**NetBIOS:** El protocolo NetBIOS se usa normalmente por los servicios de nombres en Windows. NetBIOS puede usar varios conjuntos de protocolos de red, entre los que se incluyen IP (NetBIOS sobre TCP/IP), IPX/SPX y NetBEUI. Winsock admite NetBIOS sobre TCP/IP (normalmente llamada a NetBT) solo en las versiones de 32 bits de Windows 7, Windows Server 2008 y Windows Vista. Winsock admite NetBIOS a través de TCP/IP y NetBIOS mediante IPX en Windows Server 2003 y Windows XP. Winsock admite NetBIOS a través de TCP/IP, NetBIOS mediante IPX y NetBIOS mediante NetBEUI en Windows 2000.

**IrDA:** Se admite el protocolo de Asociación de datos por infrarrojos (IrDA) si el equipo tiene instalado un puerto de infrarrojos y un controlador.

**Bluetooth:** La compatibilidad de Winsock con Bluetooth como conjunto de protocolos de red incluye los perfiles de red de área personal (PAN) y de acceso telefónico a redes (DUN) Bluetooth. La compatibilidad con Bluetooth en Windows también incluye el uso de Bluetooth Dispositivo de interfaz humana (HID) y otros perfiles para conectarse a teclados, dispositivos señaladores y otros dispositivos de entrada que no están relacionados con los protocolos de red.

**DLC en windows 2003 y Windows XP:** El protocolo de control de vínculo de datos (DLC) se admite en Windows Server 2003 y Windows XP cuando se instala el controlador DLC incluido en Microsoft Host Integration Server 2006, Host Integration Server 2004 o Host Integration Server 2000.

**ATM en windows 2003, Windows XP y windows 2000:** El protocolo de modo de transferencia asincrónico (ATM) se admite en Windows Server 2003, Windows XP y Windows 2000 cuando se instala un adaptador de red ATM. El protocolo para IP clásica sobre ATM (a veces abreviado como CLIP/ATM) se define en [RFC 2225](https://tools.ietf.org/html/rfc2225) y en los documentos relacionados publicados por IETF. Windows Server 2003, Windows XP y Windows 2000 proporcionan una implementación completa de este estándar.

**NetBEUI en Windows 2000:** El protocolo NetBEUI no es directamente compatible con Windows Sockets. Pero el protocolo NetBIOS, que puede usar varios protocolos de red, admite el uso del protocolo NetBEUI en Windows 2000.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia técnica de ATM](/previous-versions/windows/it-pro/windows-server-2003/cc759707(v=ws.10))
</dt> <dt>

[Bluetooth](../bluetooth/bluetooth-start-page.md)
</dt> <dt>

[IPv6 Technology Preview para Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Infrared](/previous-versions/windows/desktop/irda/irda-start-page)
</dt> <dt>

[Compatibilidad con NDIS 5,0 y ATM en Windows](/windows-hardware/drivers/network/ndis-version-guide)
</dt> </dl>

 

 
