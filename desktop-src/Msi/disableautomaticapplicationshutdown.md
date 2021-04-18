---
description: Si esta Directiva del sistema por equipo está establecida en 1 (uno), Windows Installer no interactúa con el administrador de reinicio, pero usará el cuadro de diálogo FilesInUse. Si esta Directiva del sistema por equipo está establecida en 2 (dos), Windows Installer utiliza el cuadro de diálogo FilesInUse.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666885"
---
# <a name="disableautomaticapplicationshutdown"></a><span data-ttu-id="c3219-103">DisableAutomaticApplicationShutdown</span><span class="sxs-lookup"><span data-stu-id="c3219-103">DisableAutomaticApplicationShutdown</span></span>

<span data-ttu-id="c3219-104">Si esta Directiva del sistema por equipo está establecida en 1 (uno), Windows Installer no interactúa con el [Administrador de reinicio](/windows/desktop/RstMgr/restart-manager-portal), pero utilizará el [cuadro de diálogo FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="c3219-104">If this per-machine system policy is set to 1 (one), Windows Installer does not interact with [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal), but it will use the [FilesInUse Dialog](filesinuse-dialog.md).</span></span>

<span data-ttu-id="c3219-105">Si esta Directiva del sistema por equipo está establecida en 2 (dos), Windows Installer usa el [cuadro de diálogo FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="c3219-105">If this per-machine system policy is set to 2 (two), Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="c3219-106">Esta configuración deshabilita los intentos del [Administrador de reinicio](/windows/desktop/RstMgr/restart-manager-portal) para mitigar los reinicios al instalar un paquete de Windows Installer que no se ha creado para usar el administrador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="c3219-106">This setting disables attempts by the [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="c3219-107">El instalador sigue usando el administrador de reinicio para detectar los archivos que usan las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c3219-107">The installer still uses the Restart Manager to detect files in use by applications.</span></span>

<span data-ttu-id="c3219-108">La Directiva DisableAutomaticApplicationShutdown está disponible a partir de Windows Installer versión 4,0 en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3219-108">The DisableAutomaticApplicationShutdown policy is available beginning with Windows Installer version 4.0 on Windows Vista.</span></span>

## <a name="registry-key"></a><span data-ttu-id="c3219-109">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="c3219-109">Registry Key</span></span>

<span data-ttu-id="c3219-110">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="c3219-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="c3219-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c3219-111">Data Type</span></span>

<span data-ttu-id="c3219-112">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="c3219-112">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3219-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3219-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3219-114">**MSIRESTARTMANAGERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="c3219-114">**MSIRESTARTMANAGERCONTROL**</span></span>](msirestartmanagercontrol.md)
</dt> <dt>

[<span data-ttu-id="c3219-115">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="c3219-115">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
