---
description: Puede usar el control InkPicture para representar la entrada de lápiz en las ediciones Microsoft Windows 2000, Windows Server 2003 y que no son de Tablet PC de Windows XP. Sin embargo, no puede usar el control para introducir entradas manuscritas en estos sistemas operativos.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Usar InkPicture en versiones anteriores de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbd2bf8545524787c9e37f70c43d954ab440910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715077"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a><span data-ttu-id="70e7e-104">Usar InkPicture en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="70e7e-104">Using InkPicture on Earlier Versions of Windows</span></span>

<span data-ttu-id="70e7e-105">Puede usar el [control InkPicture](inkpicture-control.md) para representar la entrada de lápiz en las ediciones Microsoft Windows 2000, windows Server 2003 y que no son de Tablet PC de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70e7e-105">You can use the [InkPicture Control](inkpicture-control.md) to render ink on Microsoft Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP.</span></span> <span data-ttu-id="70e7e-106">Sin embargo, no puede usar el control para introducir entradas manuscritas en estos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="70e7e-106">However, you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="70e7e-107">La propiedad [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) del control está establecida en **false** y el intento de cambiar la propiedad no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="70e7e-107">The control's [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) property is set to **FALSE**, and attempting to change the property has no effect.</span></span> <span data-ttu-id="70e7e-108">Puede asignar valores a otras propiedades y manipular la entrada mediante programación, pero no puede usar el control para recopilar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="70e7e-108">You can assign values to other properties and programmatically manipulate ink, but you cannot use the control to collect ink.</span></span>

 

 



