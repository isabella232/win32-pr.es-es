---
description: A partir de Windows Server 2008 y Windows Vista, esta directiva ya no tiene ningún efecto.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275934"
---
# <a name="enableadmintsremote"></a><span data-ttu-id="bea47-103">EnableAdminTSRemote</span><span class="sxs-lookup"><span data-stu-id="bea47-103">EnableAdminTSRemote</span></span>

<span data-ttu-id="bea47-104">A partir de Windows Server 2008 y Windows Vista, esta directiva ya no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="bea47-104">Beginning with Windows Server 2008 and Windows Vista, this policy no longer has any effect.</span></span> <span data-ttu-id="bea47-105">Un administrador puede realizar una instalación desde la sesión de consola de un servidor de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="bea47-105">An administrator can perform an installation from the console session of a terminal server.</span></span> <span data-ttu-id="bea47-106">Un administrador también puede realizar una instalación desde una sesión de cliente del servidor de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="bea47-106">An administrator can also perform an installation from a client session of the terminal server.</span></span>

<span data-ttu-id="bea47-107">Para obtener más información, vea [Terminal Services](/windows/desktop/TermServ/terminal-services-portal) en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bea47-107">For more information, see [Terminal Services](/windows/desktop/TermServ/terminal-services-portal) in the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="bea47-108">\* \* Sistemas operativos anteriores a Windows Server 2008 y Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="bea47-108">\*\*Operating systems earlier than Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="bea47-109">La configuración de esta [Directiva del sistema](system-policy.md) por equipo permite a los administradores realizar instalaciones desde una sesión de cliente del servidor de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="bea47-109">Setting this per-machine [system policy](system-policy.md) enables administrators to perform installations from a client session of the terminal server.</span></span> <span data-ttu-id="bea47-110">Si no se establece esta Directiva, los administradores solo pueden realizar instalaciones desde la sesión de consola.</span><span class="sxs-lookup"><span data-stu-id="bea47-110">If this policy is not set, administrators can only perform installations from the console session.</span></span> <span data-ttu-id="bea47-111">Los usuarios no administrativos nunca pueden realizar instalaciones desde una sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="bea47-111">Nonadministrative users can never perform installations from a client session.</span></span> <span data-ttu-id="bea47-112">El valor predeterminado de esta directiva permite que solo los administradores realicen instalaciones desde la sesión de consola.</span><span class="sxs-lookup"><span data-stu-id="bea47-112">The default value for this policy allows only administrators to perform installations from the console session.</span></span> <span data-ttu-id="bea47-113">Los administradores siempre pueden realizar [instalaciones administrativas](administrative-installation.md) desde una sesión de cliente del servidor de Terminal Server o desde la sesión de consola, independientemente de si esta directiva está establecida.</span><span class="sxs-lookup"><span data-stu-id="bea47-113">Administrators can always do [Administrative installations](administrative-installation.md) from a client session of the terminal server, or from the console session, regardless of whether this policy is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="bea47-114">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="bea47-114">Registry Key</span></span>

<span data-ttu-id="bea47-115">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="bea47-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="bea47-116">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bea47-116">Data Type</span></span>

<span data-ttu-id="bea47-117">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="bea47-117">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="bea47-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bea47-118">Remarks</span></span>

<span data-ttu-id="bea47-119">Para obtener más información, vea también [usar Windows Installer con un terminal Server](using-windows-installer-with-a-terminal-server.md).</span><span class="sxs-lookup"><span data-stu-id="bea47-119">For more information see also, [Using Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).</span></span>

 

 
