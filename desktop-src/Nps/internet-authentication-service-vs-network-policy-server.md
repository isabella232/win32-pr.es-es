---
title: Servicio de autenticación de Internet & servidor de directivas de redes
description: Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) al servidor de directivas de redes (NPS).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca657da17e823caa51e8401905a8a0a3e307e975
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104078519"
---
# <a name="internet-authentication-service--network-policy-server"></a>Servicio de autenticación de Internet & servidor de directivas de redes

Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) al servidor de directivas de redes (NPS).

## <a name="internet-authentication-service"></a>Servicio de autenticación Internet

El servicio de autenticación de Internet es la implementación de Microsoft de un servidor RADIUS y un proxy.

El servicio de autenticación de Internet admite dos conjuntos de API: [API de extensiones de servidor de directivas de redes](ias-extensions.md) y API de objetos de datos del [servidor](server-data-objects.md).

Consulte [technet: servicio de autenticación de Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obtener más información acerca de IAS.

## <a name="network-policy-server"></a>Servidor de directivas de redes

El servidor de directivas de redes es la implementación de Microsoft de un servidor RADIUS y un proxy, y está disponible en servidores de Windows a partir de Windows Server 2008.

NPS admite los mismos dos conjuntos de API que IAS: API de [extensiones de servidor de directivas de redes](ias-extensions.md) y API de objetos de datos de [servidor](server-data-objects.md).

Además, NPS contiene un conjunto de nuevas características que amplían las capacidades de IAS.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Característica</th>
<th>Novedades de NPS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/NAP/network-access-protection-start-page">Protección de acceso a redes (NAP)</a><br/></td>
<td>NPS es el servidor central de protección de acceso a redes.<br/> NPS admite la creación de directivas mediante las siguientes condiciones adicionales:<br/>
<ul>
<li>Expiración de la Directiva.</li>
<li>Versión del sistema operativo.</li>
<li>Obtener acceso a la dirección IP del cliente.</li>
<li>Directivas de mantenimiento.</li>
<li>Tipos de EAP permitidos.</li>
<li>HCAP.</li>
</ul>
NPS admite la creación de directivas con la siguiente configuración adicional:<br/>
<ul>
<li>Prueba.</li>
<li>Acceso limitado.</li>
<li>Estado extendido para el acceso limitado.</li>
</ul>
NPS, a través de NAP, interopera con CISCO NAC.<br/> IAS no es compatible con NAP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/eap/eap-start-page">EAP</a> de Compatibilidad con la Directiva y <a href="/windows/win32/eaphost/portal">EAPHost</a><br/></td>
<td>NPS usa EAPHost para la extensibilidad del método EAP. Además, los administradores pueden configurar la Directiva de acceso a la red para EAP.<br/> IAS no admite la integración de EAPHost o las condiciones de filtro de tipo de EAP para las directivas.<br/></td>
</tr>
<tr class="odd">
<td>Compatibilidad con IPv6<br/></td>
<td>NPS admite la implementación en entornos IPv6.<br/> IAS no admite direcciones de red IPv6.<br/></td>
</tr>
<tr class="even">
<td>Configuración XML<br/></td>
<td>La configuración de NPS se puede importar y exportar en formato XML.<br/> IAS está utilizando una base de datos Jet para almacenar la configuración del servicio.<br/></td>
</tr>
<tr class="odd">
<td><a href="https://www.niap-ccevs.org/cc-scheme/">Criterios comunes</a> Ser<br/></td>
<td>NPS se ha actualizado para admitir su implementación en entornos que deben cumplir los estándares de seguridad de criterios comunes.<br/></td>
</tr>
<tr class="even">
<td><a href="ias-extensions.md">API de extensiones de NPS</a><br/></td>
<td>Los archivos dll de extensión de NPS se ejecutan en un proceso independiente del servicio NPS. Si se bloquea un archivo DLL de extensión, NPS seguirá ejecutándose y se rechazarán las solicitudes futuras.<br/> Los archivos dll de extensión IAS se ejecutan en el mismo proceso que el servicio IAS y pueden afectar negativamente al servicio.<br/></td>
</tr>
<tr class="odd">
<td>Interfaz de usuario de administración<br/></td>
<td>La consola de administración de NPS (NPS. msc) tiene un nuevo aspecto y una mejor capacidad de uso, y cubre toda la nueva funcionalidad agregada a NPS.<br/> IAS usa la consola de administración de IAS. msc.<br/></td>
</tr>
<tr class="even">
<td>Herramienta de administración de roles e integración de Administrador del servidor<br/></td>
<td>NPS se integra con el Administrador del servidor y la herramienta de administración de roles. Esta integración facilita la configuración y la administración de NPS y los escenarios relacionados.<br/> Administrador del servidor no está disponible en los equipos que ejecutan IAS.<br/></td>
</tr>
<tr class="odd">
<td>Scripting de línea de comandos actualizado con <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.<br/></td>
<td>NPS es compatible con la interfaz de la &quot; línea de comandos Netsh NPS &quot; . &quot;Netsh NPS &quot; contiene nuevos comandos que permiten configurar completamente NPS, incluidas las características de NAP.<br/> IAS es compatible con la interfaz de la &quot; línea de comandos netsh aaaa &quot; .<br/></td>
</tr>
<tr class="even">
<td>Aislamiento de directivas<br/></td>
<td>NPS habilita la implementación del aislamiento de directivas estableciendo el origen de la Directiva de red. Se pueden configurar directivas que solo se aplican a un tipo de NAS predeterminado.<br/> IAS no admite el aislamiento de directivas.<br/></td>
</tr>
</tbody>
</table>



 

Consulte [technet: servidor de directivas de redes](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obtener más información sobre NPS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación, autorización y cuentas RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Registro con servidor de directivas de redes](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Trabajar con un servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

