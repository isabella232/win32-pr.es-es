---
title: Servidor de directivas de redes
description: Servidor de directivas de red (NPS) es la implementación de Microsoft de un servidor y proxy de Servicio de usuario de acceso telefónico (RADIUS) de autenticación remota.
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1f604d7cea69bcc8866176f612c76d2e6820bc4a00aa58d3760761ef59270b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362311"
---
# <a name="network-policy-server"></a>Servidor de directivas de redes

## <a name="purpose"></a>Propósito

Servidor de directivas de red (NPS) es la implementación de Microsoft de un servidor y proxy de Servicio de usuario de acceso telefónico (RADIUS) de autenticación remota. Es el sucesor del Servicio de autenticación de Internet (IAS).

Como servidor RADIUS, NPS realiza la autenticación, autorización y contabilidad de conexiones inalámbricas, de autenticación de conmutador y acceso remoto de acceso telefónico y de red privada virtual (VPN).

NPS también es un servidor evaluador de estado para protección de acceso a redes (NAP). NPS realiza la autenticación y autorización de los intentos de conexión de red y, en función de las directivas de mantenimiento del sistema configuradas, evalúa el cumplimiento del estado del equipo y determina cómo limitar el acceso o la comunicación de red de un equipo no conforme. Se trata de una nueva característica específica solo para NPS; IAS no lo admite. Consulte [Servicio de autenticación de Internet y Servidor](internet-authentication-service-vs-network-policy-server.md) de directivas de red para obtener una lista completa de las características nuevas de NPS.

NPS incluye dos conjuntos de API: NPS Extensions API y Server Data Objects (SDO) API. Tanto la API de extensiones nps como la API de SDO también son compatibles con nps, el servicio de autenticación de Internet.

NPS Extensions API se puede usar para ampliar los métodos de autenticación, autorización y contabilidad que ofrece NPS y anteriormente IAS.

Server Data Objects API se puede usar para manipular la configuración de directiva de red en un equipo que ejecuta NPS o IAS.

> [!Note]  
> Las directivas de red en NPS son equivalentes a las directivas de acceso remoto en IAS.

 

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de extensiones nps está diseñada para que la usen los programadores que usan software de desarrollo de C/C++. Los programadores deben estar familiarizados con los conceptos de red y el protocolo RADIUS. RADIUS se documenta en [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) y [RFC 2866.](https://www.ietf.org/rfc/rfc2866.txt)

Server Data Objects API está diseñada para su uso por programadores que usan C/C++ o Visual Basic de desarrollo. Los programadores deben estar familiarizados [con el Servicio de acceso](/windows/desktop/RRAS/remote-access-request-for-comments) remoto (RAS) y el protocolo RADIUS.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

NPS Extensions API se admite en Windows Server 2008 con la instalación del Servicio de Internet comercial de Microsoft (MCIS).

Server Data Objects API se admite en Windows Server 2008.

NPS está disponible en Windows Server 2008 con la instalación del Servicio de Internet comercial de Microsoft (MCIS).

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Información general](about-network-policy-server.md)
</dt> <dd>

Información general sobre RADIUS, IAS y NPS.

</dd> <dt>

[API de extensiones del servidor de directivas de red](ias-extensions.md)
</dt> <dd>

API para implementar archivos DLL de extensión que se usan para la autenticación, autorización y contabilidad.

</dd> <dt>

[Server Data Objects API](server-data-objects.md)
</dt> <dd>

API para administrar la configuración de la directiva de red.

</dd> <dt>

[SQL Programación](sql-programmability.md)
</dt> <dd>

Ejemplos de procedimientos almacenados usados para administrar el registro de NPS (IAS).

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TechNet: Servidor de directivas de red](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[TechNet: Servicio de autenticación de Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[Protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 