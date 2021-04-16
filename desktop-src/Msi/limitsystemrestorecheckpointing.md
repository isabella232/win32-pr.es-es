---
description: Esta Directiva del sistema por equipo desactiva la creación de puntos de control mediante Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686797"
---
# <a name="limitsystemrestorecheckpointing"></a><span data-ttu-id="f39a9-103">LimitSystemRestoreCheckpointing</span><span class="sxs-lookup"><span data-stu-id="f39a9-103">LimitSystemRestoreCheckpointing</span></span>

<span data-ttu-id="f39a9-104">Esta [Directiva del sistema](system-policy.md) por equipo desactiva la creación de puntos de control mediante Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f39a9-104">This per-machine [system policy](system-policy.md) turns off the creation of checkpoints by Windows Installer.</span></span>

<span data-ttu-id="f39a9-105">Si se establece en 0 o ausente, el instalador realiza un punto de comprobación normal para la instalación o desinstalación.</span><span class="sxs-lookup"><span data-stu-id="f39a9-105">Set to 0 or absent, the installer does normal checkpointing for install or uninstall.</span></span> <span data-ttu-id="f39a9-106">Si se establece en 1, el instalador no crea ningún punto de control.</span><span class="sxs-lookup"><span data-stu-id="f39a9-106">Set to 1, the installer creates no checkpoints.</span></span>

<span data-ttu-id="f39a9-107">Esta directiva solo afecta a los puntos de control establecidos por Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f39a9-107">This policy affects only checkpoints set by Windows Installer.</span></span> <span data-ttu-id="f39a9-108">En equipos con Windows XP, los administradores pueden decidir deshabilitar los puntos de comprobación desde Windows Installer para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f39a9-108">On Windows XP computers, administrators may decide to disable checkpointing from within Windows Installer to improve performance.</span></span> <span data-ttu-id="f39a9-109">[**Restaurar sistema**](../sr/system-restore-portal.md) también crea puntos de control adicionales.</span><span class="sxs-lookup"><span data-stu-id="f39a9-109">[**System Restore**](../sr/system-restore-portal.md) also creates additional checkpoints.</span></span> <span data-ttu-id="f39a9-110">Para obtener más información, vea [puntos de restauración del sistema y el Windows Installer](system-restore-points-and-the-windows-installer.md) y [establecer un punto de restauración desde una acción personalizada](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="f39a9-110">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md) and [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="f39a9-111">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="f39a9-111">Registry Key</span></span>

<span data-ttu-id="f39a9-112">Establezca el valor denominado LimitSystemRestoreCheckpointing en la siguiente clave del registro.</span><span class="sxs-lookup"><span data-stu-id="f39a9-112">Set the value named LimitSystemRestoreCheckpointing under the following registry key.</span></span>

<span data-ttu-id="f39a9-113">**HKEY \_ local \_ Machine \\ software \\ Policies \\ Microsoft \\ Windows \\ Installer**</span><span class="sxs-lookup"><span data-stu-id="f39a9-113">**HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="f39a9-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f39a9-114">Data Type</span></span>

<span data-ttu-id="f39a9-115">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="f39a9-115">**REG\_DWORD**</span></span>

 

 
