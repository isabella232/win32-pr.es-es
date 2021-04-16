---
description: Cambio posterior de la región de DVD
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Cambio posterior de la región de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a28982d6807fa5d90356d15cbf5365a595c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678365"
---
# <a name="subsequent-dvd-region-change"></a><span data-ttu-id="06dc8-103">Cambio posterior de la región de DVD</span><span class="sxs-lookup"><span data-stu-id="06dc8-103">Subsequent DVD Region Change</span></span>

<span data-ttu-id="06dc8-104">En Windows 2000 y versiones posteriores, el navegador de DVD invoca una página de propiedades en el dispositivo de unidad de DVD-ROM en el Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="06dc8-104">In Windows 2000 and later, the DVD Navigator invokes a property page on the DVD-ROM drive device in the Device Manager.</span></span> <span data-ttu-id="06dc8-105">Esta página de propiedades también la abre la aplicación DVDPlay.exe cuando es necesario cambiar una región.</span><span class="sxs-lookup"><span data-stu-id="06dc8-105">This property page is also brought up by the DVDPlay.exe application when a region needs to be changed.</span></span> <span data-ttu-id="06dc8-106">La interfaz de usuario de esta página de propiedades es muy similar a la de DVDRgn.exe y está regional en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="06dc8-106">The UI of this property page is very similar to that of DVDRgn.exe and it is regionalized in the operating system.</span></span>

<span data-ttu-id="06dc8-107">En el caso de las unidades RPC1, los componentes del sistema operativo Windows administran los cambios de la región.</span><span class="sxs-lookup"><span data-stu-id="06dc8-107">For RPC1 drives, the Windows Operating System components manage region changes.</span></span> <span data-ttu-id="06dc8-108">Las unidades RPC2 mantienen la configuración de la región en su propio hardware.</span><span class="sxs-lookup"><span data-stu-id="06dc8-108">RPC2 drives maintain the region setting in their own hardware.</span></span> <span data-ttu-id="06dc8-109">Cuando se agota el número de cambios permitidos en una unidad RPC2, la unidad no podrá realizar la llamada para cambiar la región y el componente región-cambio del sistema operativo indicará al usuario.</span><span class="sxs-lookup"><span data-stu-id="06dc8-109">When the number of allowed changes are exhausted on a RPC2 drive, the drive will fail the call to change the region and the region-change component in the operating system will indicate that to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06dc8-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06dc8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06dc8-111">Compatibilidad de cambio de región de DVD en Windows</span><span class="sxs-lookup"><span data-stu-id="06dc8-111">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



