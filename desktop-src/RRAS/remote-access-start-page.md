---
title: Acceso remoto
description: Use el Servicio de acceso remoto (RAS) para crear aplicaciones cliente.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS del servicio de acceso remoto
- RAS RAS
- Ras del servicio de acceso remoto, página de inicio
- RAS RAS, consulte Acceso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e300061c328751f288634faf2f36ab0391ba41d7079e4f42c842d31b3e29397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788290"
---
# <a name="remote-access"></a>Acceso remoto

## <a name="purpose"></a>Propósito

Use el Servicio de acceso remoto (RAS) para crear aplicaciones cliente. Estas aplicaciones muestran cuadros de diálogo comunes de RAS, administran dispositivos y conexiones de acceso remoto, y manipulan entradas de la libreta de teléfonos. RAS también proporciona la siguiente generación de funcionalidad de servidor para el Servicio de acceso remoto (RAS) para Windows. La funcionalidad del servidor RRAS sigue y se basa en el Servicio de acceso remoto (RAS).

## <a name="where-applicable"></a>Donde sea aplicable

El servicio de acceso remoto es aplicable en cualquier entorno informático que use un vínculo de red de área extensa (WAN) o una red privada virtual (VPN). RAS permite conectar un equipo cliente remoto a un servidor de red a través de un vínculo WAN o una VPN. A continuación, el equipo remoto funciona en la LAN del servidor como si el equipo remoto se conectara directamente a la LAN. La API ras permite a los programadores acceder a las características de RAS mediante programación.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API ras está diseñada para su uso por los programadores de C/C++. Los programadores Visual Basic microsoft también pueden encontrar útil la API. Los programadores deben estar familiarizados con los conceptos de red.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Algunas de las funciones de la API RAS solo se admiten en servidores de red y otras solo se admiten en clientes de red. Para obtener información más específica sobre qué sistemas operativos admiten una función determinada, consulte las secciones Requisitos de la documentación.

La [funcionalidad mejorada de RAS](function-comparison-windows-2000-versus-rras-redistributable.md) de RRAS está disponible para Windows NT Server 4.0 mediante la instalación de [RRAS redistribuible.](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp) Toda la funcionalidad de RRAS se incorpora a Windows 2000 Server, Windows Server 2003 y Windows Server 2008. Las aplicaciones RRAS no se pueden ejecutar Windows nt workstation 4.0 o en sistemas operativos cliente, como Windows 95. Para obtener información más específica sobre qué sistemas operativos admiten una función determinada, consulte las secciones Requisitos de la documentación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Servicio de acceso remoto](about-remote-access-service.md)<br/>                               | El Servicio de acceso remoto (RAS) proporciona funcionalidades de acceso remoto a las aplicaciones cliente en equipos que ejecutan Windows.<br/>                                                                                          |
| [Administración del servicio de acceso remoto](about-remote-access-service-administration.md)<br/> | Administración del servicio de acceso remoto proporciona un conjunto de funciones para administrar los permisos de usuario y los puertos en servidores RAS. Con estas funciones, puede desarrollar una aplicación de administración de servidores RAS.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enrutamiento](routing-start-page.md)
</dt> <dt>

[Protocolos de enrutamiento](routing-protocols-start-page.md)
</dt> </dl>

 

 





