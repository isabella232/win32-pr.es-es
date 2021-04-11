---
title: Acceso remoto
description: Usar el servicio de acceso remoto (RAS) para crear aplicaciones cliente.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS del servicio de acceso remoto
- RAS RAS
- RAS del servicio de acceso remoto, página de inicio
- Ras ras, consulte acceso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149102"
---
# <a name="remote-access"></a>Acceso remoto

## <a name="purpose"></a>Propósito

Usar el servicio de acceso remoto (RAS) para crear aplicaciones cliente. Estas aplicaciones muestran cuadros de diálogo comunes de RAS, administran conexiones de acceso remoto y dispositivos, y manipulan entradas de libreta de teléfonos. RAS también proporciona la siguiente generación de funcionalidad de servidor para el servicio de acceso remoto (RAS) para Windows. La funcionalidad del servidor RRAS sigue y se basa en el servicio de acceso remoto (RAS).

## <a name="where-applicable"></a>Donde sea aplicable

El servicio de acceso remoto es aplicable en cualquier entorno informático que use un vínculo de red de área extensa (WAN) o una red privada virtual (VPN). RAS permite conectar un equipo cliente remoto a un servidor de red a través de un vínculo WAN o VPN. A continuación, el equipo remoto funciona en la LAN del servidor como si el equipo remoto estuviera conectado directamente a la LAN. La API de RAS permite a los programadores tener acceso a las características de RAS mediante programación.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de RAS está diseñada para que la usen los programadores de C/C++. Los programadores de Visual Basic de Microsoft también pueden encontrar la API útil. Los programadores deben estar familiarizados con los conceptos de red.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Algunas de las funciones de la API de RAS solo se admiten en servidores de red y otras funciones solo se admiten en los clientes de red. Para obtener información más específica acerca de los sistemas operativos que admiten una función determinada, consulte las secciones de requisitos en la documentación de.

La [funcionalidad de Ras mejorada](function-comparison-windows-2000-versus-rras-redistributable.md) de RRAS está disponible para Windows NT Server 4,0 mediante la instalación del [paquete redistribuible de RRAS](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp). Toda la funcionalidad de RRAS se incorpora en Windows 2000 Server, Windows Server 2003 y Windows Server 2008. Las aplicaciones RRAS no se pueden ejecutar en Windows NT Workstation 4,0 o en sistemas operativos cliente, como Windows 95. Para obtener información más específica acerca de los sistemas operativos que admiten una función determinada, consulte las secciones de requisitos en la documentación de.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Servicio de acceso remoto](about-remote-access-service.md)<br/>                               | El servicio de acceso remoto (RAS) proporciona funciones de acceso remoto a las aplicaciones cliente en equipos que ejecutan Windows.<br/>                                                                                          |
| [Administración del servicio de acceso remoto](about-remote-access-service-administration.md)<br/> | La administración del servicio de acceso remoto proporciona un conjunto de funciones para administrar los permisos y puertos de usuario en los servidores RAS. Con estas funciones, puede desarrollar una aplicación de administración del servidor RAS.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enrutamiento](routing-start-page.md)
</dt> <dt>

[Protocolos de enrutamiento](routing-protocols-start-page.md)
</dt> </dl>

 

 





