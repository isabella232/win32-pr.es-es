---
title: Usar Teredo con la aplicación auxiliar de IP
description: Una aplicación emplea la API auxiliar de protocolo de Internet (auxiliar de IP) para recopilar y proporcionar información importante relacionada con la configuración de red del equipo local.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792508"
---
# <a name="using-teredo-with-ip-helper"></a><span data-ttu-id="60f77-103">Usar Teredo con la aplicación auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="60f77-103">Using Teredo with IP Helper</span></span>

<span data-ttu-id="60f77-104">Una aplicación emplea la API del ayudante para el [Protocolo de Internet](/windows/desktop/IpHlp/about-ip-helper) (auxiliar de IP) para recopilar y proporcionar información importante relacionada con la configuración de red del equipo local.</span><span class="sxs-lookup"><span data-stu-id="60f77-104">The [Internet Protocol Helper](/windows/desktop/IpHlp/about-ip-helper) (IP Helper) API is utilized by an application to gather and provide important information regarding the networking configuration of the local machine.</span></span> <span data-ttu-id="60f77-105">Cuando se trabaja en la plataforma de Windows Vista, esta información incluye el puerto UDP dinámico asignado a la interfaz Teredo y los cambios que se pueden producir en el puerto designado.</span><span class="sxs-lookup"><span data-stu-id="60f77-105">When operating on the Windows Vista platform, this information includes the dynamic UDP port assigned to the Teredo interface and changes that may occur to the designated port.</span></span>

<span data-ttu-id="60f77-106">La API auxiliar de IP utiliza las siguientes funciones para facilitar el uso de la interfaz Teredo:</span><span class="sxs-lookup"><span data-stu-id="60f77-106">The following functions are utilized by the IP Helper API to facilitate the use of the Teredo interface:</span></span>

-   [<span data-ttu-id="60f77-107">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="60f77-107">**GetTeredoPort**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="60f77-108">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="60f77-108">**NotifyTeredoPortChange**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="60f77-109">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="60f77-109">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 