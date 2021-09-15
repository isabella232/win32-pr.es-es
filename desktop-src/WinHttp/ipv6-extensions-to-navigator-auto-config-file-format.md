---
description: Microsoft ha implementado una matriz de extensiones en el formato de archivo de configuración automática del navegador con el fin de agregar compatibilidad con IPv6 en las funciones auxiliares de WPAD WinINet y WinHTTP.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: Extensiones IPv6 para el formato de archivo de configuración automática del navegador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b57fce93caaf7790136ee9ac7db04017d9ac11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258671"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a>Extensiones IPv6 para el formato de archivo de configuración automática del navegador

Microsoft ha implementado una matriz de extensiones en el formato de archivo de configuración automática del navegador con el fin de agregar compatibilidad con IPv6 en las funciones auxiliares de WPAD WinINet y WinHTTP.

La explosión de Internet a finales de la década de 1990 ha provocado una escasez inesperada de direcciones IPv4, con el grupo agotado diariamente. IPv6 proporciona una solución a este problema y, aunque actualmente no está ampliamente implementado, su uso será definitivamente más frecuente en el futuro. [WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) es un protocolo que permite a los clientes web detectar automáticamente cuál debe ser la configuración correcta del proxy para el tráfico saliente. Esto es muy útil para las implementaciones corporativas porque permite a los administradores de TI configurar scripts complejos que pueden enrutar el tráfico de todos los clientes a servidores proxy específicos en función del servidor de destino al que los clientes intentan conectarse. WinINet y WinHTTP admiten funciones auxiliares de WPAD, tal como se define en la especificación de formato de archivo navigator [proxy auto-config (PAC),](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html)que se ha convertido en un estándar defacto. Desafortunadamente, esta especificación se escribió en 1996 y no define cuáles deben ser los comportamientos de la función cuando se implementa un script WPAD en una red compatible con IPv6.

Puesto que IPv6 es la ola del futuro, todos los componentes de Windows ahora admiten redes de pila dual (IPv4 e IPv6) e IPv6 solo. Para admitir IPv6 sin que ello afecte a la implementación existente, Microsoft agregó 6 nuevas funciones de clase auxiliar como extensión a la especificación de formato de archivo navigator proxy auto-config (PAC) y también agregó una nueva función compatible con IPv6 denominada **FindProxyForURLEx** que los administradores pueden implementar en el script WPAD.

<dl> <dt>

[Definiciones de API del asistente de proxy compatibles con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[Diferencias entre las IPv6-Aware auxiliares de WPAD y las funciones auxiliares heredadas de WPAD](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
</dt> <dd></dd> </dl>

> [!Note]  
> Esta funcionalidad requiere Windows Internet Explorer 7 o superior.

 

 

 



