---
description: Si esta Directiva del sistema por equipo está establecida en 1, la capacidad para usar la interfaz de usuario incrustada está deshabilitada en el equipo. El valor predeterminado es 0, que habilita la capacidad de los controladores de interfaz de usuario incrustados.
ms.assetid: f69d69a3-3c28-4841-a334-3acb61a06bc2
title: MsiDisableEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f5bfe6abfbb386253631c2858dab6ef36bcf39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003047"
---
# <a name="msidisableembeddedui"></a><span data-ttu-id="197cb-104">MsiDisableEmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="197cb-104">MsiDisableEmbeddedUI</span></span>

<span data-ttu-id="197cb-105">Si esta [Directiva del sistema](system-policy.md) por equipo está establecida en 1, la capacidad para usar la interfaz de usuario incrustada está deshabilitada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="197cb-105">If this per-machine [system policy](system-policy.md) is set to 1, the capability to use embedded UI is disabled on the computer.</span></span> <span data-ttu-id="197cb-106">El valor predeterminado es 0, que habilita la capacidad de los controladores de interfaz de usuario incrustados.</span><span class="sxs-lookup"><span data-stu-id="197cb-106">The default value is 0, which enables the embedded UI handlers capability.</span></span>

<span data-ttu-id="197cb-107">Para deshabilitar la interfaz de usuario incrustada para un solo paquete, puede usar la propiedad [**MSIDISABLEEEUI**](msidisableeeui.md) .</span><span class="sxs-lookup"><span data-stu-id="197cb-107">To disable the embedded UI for a single package, you can use the [**MSIDISABLEEEUI**](msidisableeeui.md) property.</span></span>

<span data-ttu-id="197cb-108">**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="197cb-108">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="197cb-109">Esta función está disponible a partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="197cb-109">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="197cb-110">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="197cb-110">Registry Key</span></span>

<span data-ttu-id="197cb-111">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="197cb-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="197cb-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="197cb-112">Data Type</span></span>

<span data-ttu-id="197cb-113">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="197cb-113">**REG\_DWORD**</span></span>

 

 



