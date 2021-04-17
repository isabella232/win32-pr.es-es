---
description: Determine la versión de Windows Update Agent (WUA) antes de utilizarlo.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Determinar la versión actual de WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706023"
---
# <a name="determining-the-current-version-of-wua"></a><span data-ttu-id="9c226-103">Determinar la versión actual de WUA</span><span class="sxs-lookup"><span data-stu-id="9c226-103">Determining the Current Version of WUA</span></span>

<span data-ttu-id="9c226-104">Para obtener información general sobre la actualización del WUA, incluidas las instrucciones paso a paso para determinar mediante programación desde dentro de la aplicación si la versión de WUA que se está ejecutando en el equipo satisface sus necesidades, consulte [actualización del agente de Windows Update](updating-the-windows-update-agent.md).</span><span class="sxs-lookup"><span data-stu-id="9c226-104">For general information on updating the WUA, including step by step instructions to programmatically determine from within your app whether the version of WUA that is running on the computer meets your needs, see [Updating the Windows Update Agent](updating-the-windows-update-agent.md).</span></span>

<span data-ttu-id="9c226-105">En las versiones de Windows anteriores a Windows 7 y Windows Server 2008 R2, debe determinar la versión instalada de Windows Update Agent (WUA) antes de utilizarla.</span><span class="sxs-lookup"><span data-stu-id="9c226-105">On versions of Windows prior to Windows 7 and Windows Server 2008 R2, you should determine the installed version of Windows Update Agent (WUA) before you use it.</span></span> <span data-ttu-id="9c226-106">La versión actual de WUA viene determinada por la versión de la Wuaueng.dll que se ejecuta en el \\ subdirectorio system32 de la instalación actual de Windows.</span><span class="sxs-lookup"><span data-stu-id="9c226-106">The current version of WUA is determined by the version of the Wuaueng.dll that is running in the \\System32 subdirectory of the current Windows installation.</span></span> <span data-ttu-id="9c226-107">Si la versión de Wuaueng.dll es la versión 5.4.3790.1000 o una versión posterior, se instala WUA.</span><span class="sxs-lookup"><span data-stu-id="9c226-107">If the version of Wuaueng.dll is version 5.4.3790.1000 or a later version, WUA is installed.</span></span> <span data-ttu-id="9c226-108">Una versión anterior a 5.4.3790.1000 indica que el servicio de actualización de software (su) 1,0 está instalado.</span><span class="sxs-lookup"><span data-stu-id="9c226-108">A version that is earlier than 5.4.3790.1000 indicates that Software Update Services (SUS) 1.0 is installed.</span></span>

<span data-ttu-id="9c226-109">Cuando se realiza una llamada a SUS 1,0 mediante la API de WUA, se devuelve un **valor HRESULT** de Wu \_ E \_ au \_ LEGACYSERVER.</span><span class="sxs-lookup"><span data-stu-id="9c226-109">When a call is made to SUS 1.0 by using the WUA API, an **HRESULT** of WU\_E\_AU\_LEGACYSERVER is returned.</span></span>

<span data-ttu-id="9c226-110">También puede usar el método [**IWindowsUpdateAgentInfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) para recuperar la versión actual del archivo Wuapi.dll que se ejecuta en un equipo.</span><span class="sxs-lookup"><span data-stu-id="9c226-110">You can also use the [**IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) method to retrieve the current file version of Wuapi.dll that is running on a computer.</span></span> <span data-ttu-id="9c226-111">La interfaz [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) no se admite en WUA 1,0.</span><span class="sxs-lookup"><span data-stu-id="9c226-111">The [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) interface is not supported in WUA 1.0.</span></span>
