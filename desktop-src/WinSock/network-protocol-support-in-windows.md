---
description: Internet Protocol Suite es el protocolo de red dominante que se usa en redes empresariales y a través de Internet.
ms.assetid: 8c123e09-b11a-4c92-b41e-49cc01be53d3
title: Compatibilidad con el protocolo de red winsock en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36da53101dda06426a04e5f910b4548273e8ab47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474520"
---
# <a name="winsock-network-protocol-support-in-windows"></a>Compatibilidad con el protocolo de red winsock en Windows

Internet Protocol Suite es el protocolo de red dominante que se usa en redes empresariales y a través de Internet. Internet Protocol Suite representa una gran colección de protocolos de red por capas. El conjunto de protocolos de Internet se conoce a menudo como TCP/IP en función de dos de los protocolos más importantes incluidos en el conjunto: el Protocolo de Internet (IP) y el Protocolo de control de transmisión (TCP).

IPv6 e IPv4 representan las dos versiones disponibles del protocolo de Internet. TCP es uno de varios servicios de red importantes a menudo denominados protocolos IP que funcionan a través de redes IPv6 e IPv4. El Protocolo de datagramas de usuario (UDP) y el Protocolo de mensajes de control de Internet (ICMP) son otros protocolos IP importantes que se usan en redes IPv6 e IPv4. Hay varios otros protocolos IP que se pueden usar en redes IPv6 e IPv4.

Windows Sockets considera cada conjunto de protocolos de red como una familia de direcciones única. Por lo tanto, el protocolo IPv6 se considera la familia de direcciones **\_ AF INET6** y el protocolo IPv4 se considera la familia de direcciones **AF \_ INET.** Los protocolos IPv6 e IPv4 admiten el uso de varios protocolos IP por capas, como TCP, UDP e ICMP.

Windows Los sockets se diseñaron inicialmente para agregar compatibilidad con IPv4 a Windows. Sin embargo, la Windows programación de sockets de red se diseñó desde el principio con la capacidad de admitir otros conjuntos de protocolos de red. Con el tiempo, las versiones de Windows y los sockets de Windows asociados han incluido compatibilidad nativa con otros conjuntos de protocolos de red (IPX/SPX y AppleTalk, por ejemplo). La compatibilidad con otros protocolos de red también estaba disponible para las versiones de Windows software de terceros de proveedores.

Antes del crecimiento y la popularidad de Internet, se usaban otros conjuntos de protocolos de red en entornos en red, especialmente para intranets locales. La elección de un conjunto de protocolos de red a menudo se basaba en el tamaño de la red o en la experiencia del personal de redes de IT. Con la conectividad a Internet global actual que vincula incluso las redes más pequeñas al resto del mundo, la experiencia en redes en IPv6 e IPv4 es esencial para los profesionales de redes. Como resultado, otros conjuntos de protocolos de red antes importantes ahora están en un uso muy limitado y se han obviado. La compatibilidad nativa con estos conjuntos de protocolos de red obviados, a menudo denominados protocolos de red heredados, se ha eliminado de las versiones recientes de Microsoft Windows. La compatibilidad con algunos de estos protocolos heredados puede estar disponible como software de terceros de proveedores (atm con hardware de red DE CAJEROS, por ejemplo).

En la tabla siguiente se identifica la compatibilidad Windows para conjuntos de protocolos de red comunes. 

| Protocolo de red                 | Windows 7                | Windows Server 2008      | Windows Vista            | Windows Server 2003                  | Windows XP                           | Windows 2000                         |
|----------------------------------|--------------------------|--------------------------|--------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
| IPv6<br/>                  | Compatible<br/>     | Compatible<br/>     | Compatible<br/>     | Compatible<br/>                 | Compatible<br/>                 | No compatible (vea Notas)<br/> |
| IPv4<br/>                  | Compatible<br/>     | Compatible<br/>     | Compatible<br/>     | Compatible<br/>                 | Compatible<br/>                 | Compatible<br/>                 |
| NetBIOS (vea Notas) <br/>  | Compatible<br/>     | Compatible<br/>     | Compatible<br/>     | Compatible<br/>                 | Compatible<br/>                 | Compatible<br/>                 |
| IrDA (consulte notas)<br/>      | Compatible<br/>     | Compatible<br/>     | Compatible<br/>     | Compatible<br/>                 | Compatible<br/>                 | Compatible<br/>                 |
| Bluetooth (consulte notas)<br/> | Compatible<br/>     | Compatible<br/>     | Compatible<br/>     | Compatible<br/>                 | Compatible<br/>                 | No compatible<br/>             |
| IPX/SPX<br/>               | No compatible<br/> | No compatible<br/> | No compatible<br/> | Compatible<br/>                 | Compatible<br/>                 | Compatible<br/>                 |
| Appletalk<br/>             | No compatible<br/> | No compatible<br/> | No compatible<br/> | Compatible<br/>                 | Compatible<br/>                 | Compatible<br/>                 |
| DLC<br/>                   | No compatible<br/> | No compatible<br/> | No compatible<br/> | No compatible (vea Notas)<br/> | No compatible (vea Notas)<br/> | Compatible<br/>                 |
| Cajero automático<br/>                   | No compatible<br/> | No compatible<br/> | No compatible<br/> | Compatible (vea Notas)<br/>     | Compatible (vea Notas)<br/>     | Compatible (vea Notas)<br/>     |
| Netbeui<br/>               | No compatible<br/> | No compatible<br/> | No compatible<br/> | No compatible<br/>             | No compatible<br/>             | Compatible (vea Notas)<br/>     |



 

**IPv6 en Windows 2000:** El protocolo IPv6 se admite en Windows 2000 con Service Pack 1 (SP1) y versiones posteriores con Microsoft IPv6 Technology Preview para Windows 2000.

**NetBIOS:** El protocolo NetBIOS se usa normalmente mediante la asignación de nombres a los servicios Windows. NetBIOS puede usar varios conjuntos de protocolos de red, como IP (NetBIOS sobre TCP/IP), IPX/SPX y NetBEUI. Winsock admite NetBIOS sobre TCP/IP (normalmente denominado NetBT) solo en las versiones de 32 bits de Windows 7, Windows Server 2008 y Windows Vista. Winsock admite NetBIOS sobre TCP/IP y NetBIOS mediante IPX en Windows Server 2003 y Windows XP. Winsock admite NetBIOS sobre TCP/IP, NetBIOS con IPX y NetBIOS mediante NetBEUI en Windows 2000.

**IrDA:** El Protocolo de asociación de datos por infrarrojos (IrDA) (IrDA) es compatible si el equipo tiene instalado un puerto y un controlador de emergencia.

**Bluetooth:** La compatibilidad de Winsock Bluetooth como un conjunto de protocolos de red incluye los perfiles Bluetooth Personal Area Network (PAN) y Dial up Networking (DUN). Bluetooth compatibilidad con Windows también incluye el uso del dispositivo de interfaz humana (HID) de Bluetooth y otros perfiles para conectarse a teclados, dispositivos de punto y otros dispositivos de entrada que no están relacionados con los protocolos de red.

**DLC en Windows 2003 y Windows XP:** El protocolo control de vínculos de datos (DLC) se admite en Windows Server 2003 y Windows XP cuando se instala el controlador de DLC incluido con Microsoft Host Integration Server 2006, Host Integration Server 2004 o Host Integration Server 2000.

**ATM en Windows 2003, Windows XP y Windows 2000:** El protocolo modo de transferencia asincrónica (ATM) se admite en Windows Server 2003, Windows XP y Windows 2000 cuando se instala un adaptador de red de ATM. El protocolo de ip clásica sobre ATM (a veces abreviado como CLIP/ATM) se define en [RFC 2225](https://tools.ietf.org/html/rfc2225) y documentos relacionados publicados por el IETF. Windows Server 2003, Windows XP y Windows 2000 proporcionan una implementación completa de este estándar.

**NetBEUI en Windows 2000:** El protocolo NetBEUI no es compatible directamente con Windows sockets. Pero el protocolo NetBIOS que puede usar varios protocolos de red admite el uso del protocolo NetBEUI Windows 2000.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia técnica de ATM](/previous-versions/windows/it-pro/windows-server-2003/cc759707(v=ws.10))
</dt> <dt>

[Bluetooth](../bluetooth/bluetooth-start-page.md)
</dt> <dt>

[IPv6 Technology Preview para Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Irda](/previous-versions/windows/desktop/irda/irda-start-page)
</dt> <dt>

[Compatibilidad con NDIS 5.0 y ATM en Windows](/windows-hardware/drivers/network/ndis-version-guide)
</dt> </dl>

 

 
