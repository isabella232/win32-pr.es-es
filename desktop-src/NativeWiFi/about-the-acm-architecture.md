---
description: Acerca de la arquitectura ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Acerca de la arquitectura ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279005"
---
# <a name="about-the-acm-architecture"></a><span data-ttu-id="21c15-103">Acerca de la arquitectura ACM</span><span class="sxs-lookup"><span data-stu-id="21c15-103">About the ACM Architecture</span></span>

<span data-ttu-id="21c15-104">El módulo de configuración automática (ACM) es el nuevo componente de configuración inalámbrica para Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="21c15-104">The Auto Configuration Module (ACM) is the new wireless configuration component for Windows Vista.</span></span> <span data-ttu-id="21c15-105">En su lugar, Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2) usan el servicio de configuración inalámbrica rápida (WZC).</span><span class="sxs-lookup"><span data-stu-id="21c15-105">Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) use the Wireless Zero Configuration (WZC) service instead.</span></span>

<span data-ttu-id="21c15-106">ACM examina las redes periódicamente y usa un proceso iterativo para seleccionar y conectarse a la red más preferida en el intervalo, si esa red tiene una interfaz habilitada para la conexión automática.</span><span class="sxs-lookup"><span data-stu-id="21c15-106">The ACM scans networks periodically and uses an iterative process to select and connect to the most preferred network in the range, if that network has an interface enabled for auto-connection.</span></span> <span data-ttu-id="21c15-107">ACM también guarda y recupera perfiles de red, que contienen la configuración de ACM, el módulo específico de medios (MSM), la seguridad y la configuración de proveedor de hardware independiente (IHV).</span><span class="sxs-lookup"><span data-stu-id="21c15-107">The ACM also saves and retrieves network profiles, which contain ACM, Media Specific Module (MSM), security, and independent hardware vendor (IHV) settings.</span></span> <span data-ttu-id="21c15-108">Estos perfiles de red son para la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="21c15-108">These network profiles are for auto configuration.</span></span>

<span data-ttu-id="21c15-109">La configuración automática es compatible con los perfiles de red y la configuración global y por interfaz.</span><span class="sxs-lookup"><span data-stu-id="21c15-109">Auto configuration supports both global and per-interface settings and network profiles.</span></span> <span data-ttu-id="21c15-110">La configuración global y los perfiles de red se configuran si el equipo se ha unido a un dominio con un objeto de directiva de grupo (GPO) en el nivel de dominio o en el nivel de unidad organizativa (OU) de la jerarquía de Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="21c15-110">The global settings and network profiles are configured if the machine has joined a domain with a group policy object (GPO) either at the domain level or the organizational unit (OU) level in the Active Directory (AD) hierarchy.</span></span> <span data-ttu-id="21c15-111">Estos perfiles y la configuración de directiva de grupo son de solo lectura, se aplican a cada interfaz 802,11 en el sistema y siempre tienen prioridad sobre la configuración por interfaz y los perfiles de red y la configuración por usuario.</span><span class="sxs-lookup"><span data-stu-id="21c15-111">These group policy settings and profiles are read-only, applied to each 802.11 interface in the system, and always take precedence over the per-interface and per-user settings and network profiles.</span></span> <span data-ttu-id="21c15-112">Los perfiles de directiva de grupo se colocan en la parte superior de la lista de perfiles de red preferidos en cada interfaz de red 802,11.</span><span class="sxs-lookup"><span data-stu-id="21c15-112">The group policy profiles are placed at the top of the preferred network profile list on each 802.11 network interface.</span></span>

<span data-ttu-id="21c15-113">La arquitectura ACM es extensible.</span><span class="sxs-lookup"><span data-stu-id="21c15-113">The ACM architecture is extensible.</span></span> <span data-ttu-id="21c15-114">Los IHV pueden implementar la funcionalidad inalámbrica de propiedad sin modificar el marco 802,11 nativo proporcionado.</span><span class="sxs-lookup"><span data-stu-id="21c15-114">IHVs can implement proprietary wireless functionality without altering the provided native 802.11 framework.</span></span> <span data-ttu-id="21c15-115">Las estructuras y funciones de control de IHV expuestas habilitan esta extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="21c15-115">The exposed IHV control functions and structures enable this extensibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21c15-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="21c15-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21c15-117">Acerca de WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="21c15-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 



