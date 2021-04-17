---
description: Microsoft ha implementado una matriz de extensiones para el formato de archivo de configuración automática del navegador con el fin de agregar compatibilidad con IPv6 en las funciones auxiliares de WPAD de WinINet y WinHTTP.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: Extensiones IPv6 para el formato de archivo de configuración automática de navegador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b57fce93caaf7790136ee9ac7db04017d9ac11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688310"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a>Extensiones IPv6 para el formato de archivo de configuración automática de navegador

Microsoft ha implementado una matriz de extensiones para el formato de archivo de configuración automática del navegador con el fin de agregar compatibilidad con IPv6 en las funciones auxiliares de WPAD de WinINet y WinHTTP.

La explosión de Internet a finales de 1990 ha provocado un escasez inesperado de direcciones IPv4, y el grupo se está agotando diariamente. IPv6 proporciona una solución a este problema y, aunque actualmente no está ampliamente implementada, su uso se hará más frecuente en el futuro. [WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) es un protocolo que permite a los clientes Web detectar automáticamente cuál debe ser la configuración de proxy correcta para su tráfico de salida. Esto es muy útil para las implementaciones corporativas, ya que permite a los administradores de ti configurar scripts complejos que pueden enrutar el tráfico de todos los clientes a servidores proxy específicos en función del servidor de destino al que los clientes intentan conectarse. WinINet y WinHTTP admiten funciones auxiliares de WPAD, tal como se define en la [especificación de formato de archivo de configuración automática de proxy de navegador (PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), que se ha convertido en un estándar de facto. Desafortunadamente, esta especificación se escribió en 1996 y no define lo que debe ser el comportamiento de la función cuando se implementa un script WPAD en una red compatible con IPv6.

Dado que IPv6 es la ola del futuro, todos los componentes de Windows admiten ahora redes de pila dual (IPv4 e IPv6) e IPv6. Con el fin de admitir IPv6 sin afectar a la implementación existente, Microsoft ha agregado 6 nuevas funciones de clase auxiliar como extensión a la especificación de formato de archivo de configuración automática de proxy de navegador (PAC) y también ha agregado una nueva función compatible con IPv6 denominada **FindProxyForURLEx** que los administradores pueden implementar en el script WPAD.

<dl> <dt>

[Definiciones de API de aplicación auxiliar de proxy compatible con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[Diferencias entre las funciones auxiliares de WPAD IPv6-Aware y las funciones auxiliares de WPAD heredadas](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
</dt> <dd></dd> </dl>

> [!Note]  
> Esta funcionalidad requiere Windows Internet Explorer 7 o posterior.

 

 

 



