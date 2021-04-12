---
title: Servidor de directivas de redes
description: El servidor de directivas de redes (NPS) es la implementación de Microsoft de un servidor y proxy de servicio de autenticación remota telefónica de usuario (RADIUS).
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359076"
---
# <a name="network-policy-server"></a>Servidor de directivas de redes

## <a name="purpose"></a>Propósito

El servidor de directivas de redes (NPS) es la implementación de Microsoft de un servidor y proxy de servicio de autenticación remota telefónica de usuario (RADIUS). Es el sucesor del servicio de autenticación de Internet (IAS).

Como servidor RADIUS, NPS realiza la autenticación, la autorización y la administración de cuentas para conexiones de acceso remoto y de acceso telefónico y de red privada virtual (VPN).

NPS también es un servidor de evaluador de estado para protección de acceso a redes (NAP). NPS realiza la autenticación y autorización de los intentos de conexión de red y, según las directivas de mantenimiento del sistema configuradas, evalúa el cumplimiento del estado del equipo y determina cómo limitar el acceso o la comunicación de red de un equipo no compatible. Se trata de una característica nueva específica de NPS únicamente; IAS no lo admite. Consulte [servicio de autenticación de Internet y servidor de directivas de redes](internet-authentication-service-vs-network-policy-server.md) para obtener una lista completa de las características nuevas de NPS.

NPS incluye dos conjuntos de API: API de extensiones de NPS y API de objetos de datos de servidor (SDO). El precursor de NPS, el servicio de autenticación de Internet, también admiten la API de extensiones de NPS y la API SDO.

La API de extensiones de NPS se puede usar para ampliar los métodos de autenticación, autorización y cuentas ofrecidos por NPS y antes por IAS.

La API de objetos de datos del servidor se puede usar para manipular la configuración de la Directiva de red en un equipo que ejecuta NPS o IAS.

> [!Note]  
> Las directivas de red en NPS son equivalentes a las directivas de acceso remoto en IAS.

 

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de extensiones de NPS está diseñada para que la usen los programadores con el software de desarrollo de C/C++. Los programadores deben estar familiarizados con los conceptos de red y el protocolo RADIUS. RADIUS se documenta en [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) y [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

La API de objetos de datos del servidor está diseñada para que la usen los programadores que usan C/C++ o el software de desarrollo de Visual Basic. Los programadores deben estar familiarizados con el [servicio de acceso remoto](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) y el protocolo RADIUS.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API de extensiones de NPS se admite en Windows Server 2008 con la instalación del servicio Microsoft Commercial Internet (MCIS).

Server Data Objects API es compatible con Windows Server 2008.

NPS está disponible en Windows Server 2008 con la instalación del servicio Microsoft Commercial Internet (MCIS).

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Información general](about-network-policy-server.md)
</dt> <dd>

Información general relacionada con RADIUS, IAS y NPS.

</dd> <dt>

[API de extensiones de servidor de directivas de redes](ias-extensions.md)
</dt> <dd>

API para implementar archivos dll de extensión que se usan para la autenticación, autorización y cuentas.

</dd> <dt>

[Server Data Objects API](server-data-objects.md)
</dt> <dd>

API para administrar la configuración de la Directiva de red.

</dd> <dt>

[Programación de SQL](sql-programmability.md)
</dt> <dd>

Ejemplos de procedimientos almacenados que se usan para administrar el registro de NPS (IAS).

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TechNet: servidor de directivas de redes](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[TechNet: servicio de autenticación de Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[Protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 