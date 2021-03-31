---
description: La Directiva de inicio de sesión automático (inicio de sesión automático) determina cuándo es aceptable que WinHTTP incluya las credenciales predeterminadas en una solicitud al servidor.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: WinHttpAutoLogonLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910670"
---
# <a name="winhttpautologonlevel"></a><span data-ttu-id="0b4f8-103">WinHttpAutoLogonLevel</span><span class="sxs-lookup"><span data-stu-id="0b4f8-103">WinHttpAutoLogonLevel</span></span>

<span data-ttu-id="0b4f8-104">La Directiva de inicio de sesión automático (inicio de sesión automático) determina cuándo es aceptable que *WinHTTP* incluya las credenciales predeterminadas en una solicitud al servidor.</span><span class="sxs-lookup"><span data-stu-id="0b4f8-104">The automatic logon (auto-logon) policy determines when it is acceptable for *WinHTTP* to include the default credentials in a request to the server.</span></span>

<span data-ttu-id="0b4f8-105">Puede establecer este valor en **L** para el **\_ nivel de seguridad de inicio de sesión automático de \_ \_ \_ WinHTTP**, establecido en **M** para el **nivel de seguridad de inicio de \_ sesión automático \_ \_ \_ de WinHTTP**, y establecido en **H** para el **nivel de seguridad de inicio de \_ sesión automático de WinHTTP \_ \_ \_ alto**.</span><span class="sxs-lookup"><span data-stu-id="0b4f8-105">You can set this value to **L** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW**, set to **M** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**, and set to **H** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH**.</span></span> <span data-ttu-id="0b4f8-106">El nivel predeterminado es **el \_ \_ nivel de seguridad de \_ \_ Inicio de sesión automático de WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="0b4f8-106">The default level is **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**.</span></span> <span data-ttu-id="0b4f8-107">Para obtener más información acerca de la Directiva de inicio de sesión automático, consulte la sección para la [autenticación en WinHTTP](../winhttp/authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="0b4f8-107">For more information about automatic logon policy, see the section for [Authentication in WinHTTP](../winhttp/authentication-in-winhttp.md).</span></span>

<span data-ttu-id="0b4f8-108">**Windows 8 y Windows Server 2012:** Esta directiva requiere Windows Installer que se ejecuten en Windows 8 o Windows Server 2012 y no está disponible en todas las versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="0b4f8-108">**Windows 8 and Windows Server 2012:** This policy requires Windows Installer running on the Windows 8 or Windows Server 2012 and is unavailable on all earlier versions of Windows.</span></span>

## <a name="registry-key"></a><span data-ttu-id="0b4f8-109">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="0b4f8-109">Registry Key</span></span>

<span data-ttu-id="0b4f8-110">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="0b4f8-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="0b4f8-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0b4f8-111">Data Type</span></span>

<span data-ttu-id="0b4f8-112">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="0b4f8-112">**REG\_SZ**</span></span>

 

 
