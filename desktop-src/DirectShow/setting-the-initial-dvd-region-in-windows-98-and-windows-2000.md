---
description: Configuración de la región de DVD inicial
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Configuración de la región de DVD inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3f5181b804a9d83c04eed0abc70095bf9f1cf2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536442"
---
# <a name="setting-the-initial-dvd-region"></a><span data-ttu-id="73876-103">Configuración de la región de DVD inicial</span><span class="sxs-lookup"><span data-stu-id="73876-103">Setting the Initial DVD Region</span></span>

<span data-ttu-id="73876-104">Es responsabilidad del fabricante del sistema seleccionar una región de DVD inicial para la unidad de DVD en sus equipos.</span><span class="sxs-lookup"><span data-stu-id="73876-104">It is the responsibility of the system manufacturer to select an initial DVD region for the DVD drive in their PCs.</span></span>

> [!Note]  
> <span data-ttu-id="73876-105">Solo se pueden usar discos cifrados para establecer la región.</span><span class="sxs-lookup"><span data-stu-id="73876-105">Only encrypted discs can be used to set the region.</span></span>

 

### <a name="windows-2000-and-later"></a><span data-ttu-id="73876-106">Windows 2000 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="73876-106">Windows 2000 and Later</span></span>

<span data-ttu-id="73876-107">A partir de Windows 2000, se selecciona la región de DVD predeterminada en función de la configuración regional para la que esté configurada la máquina.</span><span class="sxs-lookup"><span data-stu-id="73876-107">Starting in Windows 2000, the default DVD region is selected based upon the locale that the machine is set up for.</span></span> <span data-ttu-id="73876-108">Windows 2000 siempre establecerá la región inicial de una unidad de DVD usando esta región predeterminada, así como la región del disco, si hay un disco en la unidad.</span><span class="sxs-lookup"><span data-stu-id="73876-108">Windows 2000 will always set the initial region for a DVD drive using this default region as well as the disc's region, if there is a disc is in the drive.</span></span> <span data-ttu-id="73876-109">El fabricante del sistema no tiene que hacer nada para establecer la región inicial de las unidades de DVD de Windows 2000 o posterior.</span><span class="sxs-lookup"><span data-stu-id="73876-109">The system manufacturer does not have to do anything to set the initial region for Windows 2000 or later DVD drives.</span></span>

<span data-ttu-id="73876-110">En el caso de las unidades de RPC1, si no hay ningún disco en la unidad durante el arranque, la región predeterminada se establece según la configuración regional de la máquina.</span><span class="sxs-lookup"><span data-stu-id="73876-110">For RPC1 drives, if there is no disc in the drive during boot up then the default region is set based only on the locale of the machine.</span></span> <span data-ttu-id="73876-111">Si hay un disco DVD en la unidad durante el arranque, se selecciona la región predeterminada para que sea la región de la unidad, siempre que coincida con una región del disco; de lo contrario, se selecciona la región más baja del disco como la región inicial de la unidad.</span><span class="sxs-lookup"><span data-stu-id="73876-111">If there is a DVD disc in the drive during boot up, the default region is selected to be the drive's region, provided it matches a region of the disc; otherwise the lowest region on the disc is picked as the initial region of the drive.</span></span> <span data-ttu-id="73876-112">El usuario (o fabricante del sistema) tiene permitido un cambio restante, en caso de que el valor predeterminado no sea correcto.</span><span class="sxs-lookup"><span data-stu-id="73876-112">The user (or system manufacturer) has one remaining change allowed, in case the default was not correct.</span></span>

<span data-ttu-id="73876-113">En el caso de las unidades de RPC2, si durante el proceso de instalación Windows 2000 detecta que la unidad no tiene ninguna región establecida, intentará seleccionar una región como la anterior, pero solo si hay un disco en la unidad.</span><span class="sxs-lookup"><span data-stu-id="73876-113">For RPC2 drives, if during the setup process Windows 2000 finds that the drive does not have any region set, it will try to pick a region as above, but only if there is a disc in the drive.</span></span> <span data-ttu-id="73876-114">(Las unidades de RPC1 elegirán la región sin ningún disco en la unidad).</span><span class="sxs-lookup"><span data-stu-id="73876-114">(RPC1 drives will choose the region without any disc in drive).</span></span> <span data-ttu-id="73876-115">Una vez que se establece una región para las unidades de RPC2, no se cambia automáticamente mediante una reinstalación o una instalación limpia del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="73876-115">Once a region is set for RPC2 drives, it is not auto-changed by either a re-installation or a clean installation of the Operating System.</span></span>

<span data-ttu-id="73876-116">El OEM puede establecer una clave del registro que contenga la región de DVD predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="73876-116">The OEM can set a registry key containing the default DVD region for the system.</span></span> <span data-ttu-id="73876-117">En el primer arranque, la región de la unidad se establecerá en este valor.</span><span class="sxs-lookup"><span data-stu-id="73876-117">On first boot, the drive region will be set to this value.</span></span> <span data-ttu-id="73876-118">La clave del registro en Windows 2000 y versiones posteriores es HKLM \\ System \\ CurrentControlSet \\ control \\ Class \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion (Binary).</span><span class="sxs-lookup"><span data-stu-id="73876-118">The registry key on Windows 2000 and later is HKLM\\System\\CurrentControlSet\\Control\\Class\\<CDROM GUID>\\ <instance number>\\DefaultDVDRegion(binary) .</span></span>

## <a name="related-topics"></a><span data-ttu-id="73876-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73876-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73876-120">Compatibilidad de cambio de región de DVD en Windows</span><span class="sxs-lookup"><span data-stu-id="73876-120">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



