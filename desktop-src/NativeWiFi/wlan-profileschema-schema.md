---
description: Define un perfil de WLAN usado por el servicio de configuración automática de WiFi nativo.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: Esquema de WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154107"
---
# <a name="wlan_profile-schema"></a><span data-ttu-id="5fef3-103">Esquema de Perfil de WLAN \_</span><span class="sxs-lookup"><span data-stu-id="5fef3-103">WLAN\_profile Schema</span></span>

<span data-ttu-id="5fef3-104">El esquema de Perfil de WLAN \_ define un perfil de WLAN que usa el servicio de configuración automática de WiFi nativo.</span><span class="sxs-lookup"><span data-stu-id="5fef3-104">The WLAN\_profile Schema defines a WLAN profile used by the Native Wifi AutoConfig service.</span></span>

<span data-ttu-id="5fef3-105">El servicio de configuración automática acepta perfiles inalámbricos del agente de directiva de grupo, la interfaz de scripting (**netsh**), la interfaz de usuario o la interfaz de configuración Flash de USB.</span><span class="sxs-lookup"><span data-stu-id="5fef3-105">The AutoConfig service accepts wireless profiles from the Group Policy Agent, the scripting interface (**netsh**), the user interface, or from the USB flash configuration interface.</span></span>

<span data-ttu-id="5fef3-106">Un perfil recibido de uno de estos sistemas se asigna al esquema de \_ Perfil de WLAN y se almacena en el almacén de perfiles.</span><span class="sxs-lookup"><span data-stu-id="5fef3-106">A profile received from one of these systems is mapped to the WLAN\_profile schema and stored in the profile store.</span></span> <span data-ttu-id="5fef3-107">Los perfiles se pueden exportar desde el almacén de perfiles mediante comandos Netsh o mediante elementos de la API como [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span><span class="sxs-lookup"><span data-stu-id="5fef3-107">Profiles can be exported from the profile store using netsh commands or using API elements such as [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span></span>

<span data-ttu-id="5fef3-108">El elemento raíz de un perfil de WLAN es el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5fef3-108">The root element of a WLAN profile is the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span> <span data-ttu-id="5fef3-109">Cada perfil tendrá exactamente un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="5fef3-109">Each profile will have exactly one root element.</span></span> <span data-ttu-id="5fef3-110">El elemento **WLANProfile** se encuentra en el espacio de nombres `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="5fef3-110">The **WLANProfile** element is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

<span data-ttu-id="5fef3-111">Para ver los perfiles de WLAN de ejemplo, consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="5fef3-111">To view sample WLAN profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

-   [<span data-ttu-id="5fef3-112">Elementos de esquema de Perfil de WLAN \_</span><span class="sxs-lookup"><span data-stu-id="5fef3-112">WLAN\_profile Schema Elements</span></span>](wlan-profileschema-elements.md)
-   [<span data-ttu-id="5fef3-113">\_Tipos simples de esquema de Perfil de WLAN</span><span class="sxs-lookup"><span data-stu-id="5fef3-113">WLAN\_profile Schema Simple Types</span></span>](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a><span data-ttu-id="5fef3-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5fef3-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5fef3-115">[Comandos Netsh para la red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="5fef3-115">[Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span></span>
</dt> </dl>

 

 
