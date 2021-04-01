---
title: Entradas del registro (COM)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 'Más información acerca de: entradas del registro (COM)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153472"
---
# <a name="registry-entries-com"></a><span data-ttu-id="1efd5-103">Entradas del registro (COM)</span><span class="sxs-lookup"><span data-stu-id="1efd5-103">Registry Entries (COM)</span></span>

<span data-ttu-id="1efd5-104">Los valores del registro en las siguientes claves del registro controlan aspectos de la funcionalidad de COM:</span><span class="sxs-lookup"><span data-stu-id="1efd5-104">Registry values in the following registry keys control aspects of the functionality of COM:</span></span>

-   [<span data-ttu-id="1efd5-105">**HKEY \_ \_ clases de \\ software de máquina local \\**</span><span class="sxs-lookup"><span data-stu-id="1efd5-105">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**</span></span>](hkey-local-machine-software-classes.md)
-   [<span data-ttu-id="1efd5-106">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**</span><span class="sxs-lookup"><span data-stu-id="1efd5-106">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Ole**</span></span>](hkey-local-machine-software-microsoft-ole.md)
-   [<span data-ttu-id="1efd5-107">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="1efd5-107">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

<span data-ttu-id="1efd5-108">A partir de Windows Server 2003, COM usa solo el token de proceso actual para decidir a qué subárbol del registro acceder, no el token de subproceso.</span><span class="sxs-lookup"><span data-stu-id="1efd5-108">As of Windows Server 2003, COM uses only the current process token to decide which registry hive to access, not the thread token.</span></span> <span data-ttu-id="1efd5-109">Si COM no puede tener acceso al subárbol del registro del perfil de usuario, tendrá acceso al subárbol del **\_ \_ \\ sistema del equipo local HKEY** .</span><span class="sxs-lookup"><span data-stu-id="1efd5-109">If COM is not able to access the user profile registry hive, it will access the **HKEY\_LOCAL\_MACHINE\\System** hive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1efd5-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1efd5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1efd5-111">Registro</span><span class="sxs-lookup"><span data-stu-id="1efd5-111">Registry</span></span>](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
