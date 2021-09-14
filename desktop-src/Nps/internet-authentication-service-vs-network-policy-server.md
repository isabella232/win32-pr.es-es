---
title: Servicio de autenticación de Internet & servidor de directivas de red
description: Obtenga información sobre el servicio de autenticación de Internet y el servidor de directivas de red. El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36751c66b525749afce0d5546f61fa35c1cbb856
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071516"
---
# <a name="internet-authentication-service--network-policy-server"></a>Servicio de autenticación de Internet & servidor de directivas de red

El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS).

## <a name="internet-authentication-service"></a>Servicio de autenticación Internet

El servicio de autenticación de Internet es la implementación de Microsoft de un servidor RADIUS y un proxy.

El servicio de autenticación de Internet admite dos conjuntos de [API: Network Policy Server Extensions API](ias-extensions.md) y [Server Data Objects API](server-data-objects.md).

Consulte [TechNet: Servicio de autenticación de Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obtener más información sobre IAS.

## <a name="network-policy-server"></a>Servidor de directivas de redes

Servidor de directivas de red es la implementación de Microsoft de un servidor RADIUS y proxy y está disponible en servidores Windows a partir de Windows Server 2008.

NPS admite los mismos dos conjuntos de API que IAS: NETWORK [Policy Server Extensions API](ias-extensions.md) y Server Data Objects [API](server-data-objects.md).

Además, NPS contiene un conjunto de nuevas características que amplían las funcionalidades de IAS.




| Característica | Novedades de NPS | 
|---------|--------------------|
| <a href="/windows/desktop/NAP/network-access-protection-start-page">Protección de acceso a redes (NAP)</a><br /> | NPS es el servidor central de Protección de acceso a redes.<br /> NPS admite la creación de directivas mediante las siguientes condiciones adicionales:<br /><ul><li>Expiración de la directiva.</li><li>Versión del sistema operativo.</li><li>Acceda a la dirección IP del cliente.</li><li>Directivas de mantenimiento.</li><li>Tipos de EAP permitidos.</li><li>HCAP.</li></ul>NPS admite la creación de directivas mediante la siguiente configuración adicional:<br /><ul><li>Libertad condicional.</li><li>Acceso limitado.</li><li>Estado extendido para acceso limitado.</li></ul>NPS, a través de NAP, interopera con CISCO NAC.<br /> IAS no admite NAP.<br /> | 
| <a href="/windows/win32/eap/eap-start-page">EAP</a> Compatibilidad con <a href="/windows/win32/eaphost/portal">directivas y EAPHost</a><br /> | NPS usa EAPHost para la extensibilidad del método EAP. Además, los administradores pueden configurar la directiva de acceso de red para EAP.<br /> IAS no admite la integración de EAPHost ni condiciones de filtro de tipo EAP para las directivas.<br /> | 
| Compatibilidad con IPv6<br /> | NPS admite la implementación en entornos IPv6.<br /> IAS no admite direcciones de red IPv6.<br /> | 
| Configuración XML<br /> | La configuración de NPS se puede importar y exportar en formato XML.<br /> IAS usa una base de datos Jet para almacenar la configuración del servicio.<br /> | 
| <a href="https://www.niap-ccevs.org/cc-scheme/">Criterios comunes</a> Apoyo<br /> | NPS se ha actualizado para admitir su implementación en entornos que deben cumplir los estándares de seguridad de Common Criteria.<br /> | 
| <a href="ias-extensions.md">NPS Extensions API</a><br /> | Los archivos DLL de extensión NPS se ejecutan en un proceso independiente del servicio NPS. Si se bloquea un archivo DLL de extensión, NPS seguirá ejecutándose y se rechazarán las solicitudes futuras.<br /> Los archivos DLL de extensión IAS se ejecutan en el mismo proceso que el servicio IAS y pueden afectar negativamente al servicio.<br /> | 
| Administración Interfaz de usuario<br /> | La consola de administración de NPS (nps.msc) tiene un aspecto nuevo, mejora la facilidad de uso y cubre todas las nuevas funcionalidades agregadas a NPS.<br /> IAS usa la consola de administración de ias.msc.<br /> | 
| Herramienta de administración de roles e Administrador del servidor integración<br /> | NPS se integra con el Administrador del servidor y la herramienta de administración de roles. Esta integración facilita la configuración y administración de NPS y escenarios relacionados.<br /> Administrador del servidor no está disponible en equipos que ejecutan IAS.<br /> | 
| Se ha actualizado el scripting de línea de comandos <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">con Netsh</a>.<br /> | NPS admite la interfaz de línea de comandos "Netsh nps". "Netsh nps" contiene nuevos comandos que permiten configurar completamente NPS, incluidas las características de NAP.<br /> IAS admite la interfaz de línea de comandos "Netsh aaaa".<br /> | 
| Aislamiento de directivas<br /> | NPS habilita la implementación del aislamiento de directiva estableciendo el origen de la directiva de red. Se pueden configurar directivas que solo son aplicables a un tipo DE NAS predeterminado.<br /> IAS no admite el aislamiento de directivas.<br /> | 




 

Consulte [TechNet: Servidor de directivas de red](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obtener más información sobre NPS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación, autorización y contabilidad RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Registro con el servidor de directivas de red](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Trabajar con un servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

