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
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a><span data-ttu-id="abc2b-103">Extensiones IPv6 para el formato de archivo de configuración automática de navegador</span><span class="sxs-lookup"><span data-stu-id="abc2b-103">IPv6 Extensions to Navigator Auto-Config File Format</span></span>

<span data-ttu-id="abc2b-104">Microsoft ha implementado una matriz de extensiones para el formato de archivo de configuración automática del navegador con el fin de agregar compatibilidad con IPv6 en las funciones auxiliares de WPAD de WinINet y WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="abc2b-104">Microsoft has implemented an array of extensions to the Navigator Auto-Config File Format in order to add IPv6 support in the WinINet and WinHTTP WPAD helper functions.</span></span>

<span data-ttu-id="abc2b-105">La explosión de Internet a finales de 1990 ha provocado un escasez inesperado de direcciones IPv4, y el grupo se está agotando diariamente.</span><span class="sxs-lookup"><span data-stu-id="abc2b-105">The explosion of the Internet in the late 1990’s has caused an unexpected scarcity of IPv4 addresses, with the pool depleting on a daily basis.</span></span> <span data-ttu-id="abc2b-106">IPv6 proporciona una solución a este problema y, aunque actualmente no está ampliamente implementada, su uso se hará más frecuente en el futuro.</span><span class="sxs-lookup"><span data-stu-id="abc2b-106">IPv6 provides a solution to this problem and although it is currently not widely deployed, its use will definitely become more prevalent in the future.</span></span> <span data-ttu-id="abc2b-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) es un protocolo que permite a los clientes Web detectar automáticamente cuál debe ser la configuración de proxy correcta para su tráfico de salida.</span><span class="sxs-lookup"><span data-stu-id="abc2b-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) is a protocol that allows web clients to automatically detect what the correct proxy configuration should be for their outgoing traffic.</span></span> <span data-ttu-id="abc2b-108">Esto es muy útil para las implementaciones corporativas, ya que permite a los administradores de ti configurar scripts complejos que pueden enrutar el tráfico de todos los clientes a servidores proxy específicos en función del servidor de destino al que los clientes intentan conectarse.</span><span class="sxs-lookup"><span data-stu-id="abc2b-108">This is very useful for corporate deployments because it allows IT administrators to setup complex scripts that can route traffic for all clients to specific proxies based on the target server the clients are attempting to connect to.</span></span> <span data-ttu-id="abc2b-109">WinINet y WinHTTP admiten funciones auxiliares de WPAD, tal como se define en la [especificación de formato de archivo de configuración automática de proxy de navegador (PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), que se ha convertido en un estándar de facto.</span><span class="sxs-lookup"><span data-stu-id="abc2b-109">WinINet and WinHTTP support WPAD helper functions as defined by the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), which has become a defacto standard.</span></span> <span data-ttu-id="abc2b-110">Desafortunadamente, esta especificación se escribió en 1996 y no define lo que debe ser el comportamiento de la función cuando se implementa un script WPAD en una red compatible con IPv6.</span><span class="sxs-lookup"><span data-stu-id="abc2b-110">Unfortunately this specification was written in 1996 and does not define what the function behaviors should be when a WPAD script is deployed in an IPv6 capable network.</span></span>

<span data-ttu-id="abc2b-111">Dado que IPv6 es la ola del futuro, todos los componentes de Windows admiten ahora redes de pila dual (IPv4 e IPv6) e IPv6.</span><span class="sxs-lookup"><span data-stu-id="abc2b-111">Since IPv6 is the wave of the future, all Windows components now support dual stack (IPv4 and IPv6) and IPv6 only networks.</span></span> <span data-ttu-id="abc2b-112">Con el fin de admitir IPv6 sin afectar a la implementación existente, Microsoft ha agregado 6 nuevas funciones de clase auxiliar como extensión a la especificación de formato de archivo de configuración automática de proxy de navegador (PAC) y también ha agregado una nueva función compatible con IPv6 denominada **FindProxyForURLEx** que los administradores pueden implementar en el script WPAD.</span><span class="sxs-lookup"><span data-stu-id="abc2b-112">In order to support IPv6 without affecting existing deployment, Microsoft added 6 new helper class functions as an extension to the Navigator Proxy Auto-Config (PAC) File Format specification and also added a new IPv6 capable function called **FindProxyForURLEx** that administrators can implement in the WPAD script.</span></span>

<dl> <dt>

[<span data-ttu-id="abc2b-113">Definiciones de API de aplicación auxiliar de proxy compatible con IPv6</span><span class="sxs-lookup"><span data-stu-id="abc2b-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[<span data-ttu-id="abc2b-114">Diferencias entre las funciones auxiliares de WPAD IPv6-Aware y las funciones auxiliares de WPAD heredadas</span><span class="sxs-lookup"><span data-stu-id="abc2b-114">Differences Between IPv6-Aware WPAD Helper Functions and Legacy WPAD Helper Functions</span></span>](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
<span data-ttu-id="abc2b-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="abc2b-115"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="abc2b-116">Esta funcionalidad requiere Windows Internet Explorer 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="abc2b-116">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



