---
description: Los binarios de Windows Server 2003 con Service Pack 1 (SP1) son compatibles con Windows Vista y Windows Server 2008. Sin embargo, se deben volver a compilar los archivos binarios de versiones anteriores de Windows.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Trasladar aplicaciones de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544971"
---
# <a name="porting-backup-applications"></a><span data-ttu-id="13948-104">Trasladar aplicaciones de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="13948-104">Porting Backup Applications</span></span>

<span data-ttu-id="13948-105">Los binarios de Windows Server 2003 con Service Pack 1 (SP1) son compatibles con Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="13948-105">Binaries from Windows Server 2003 with Service Pack 1 (SP1) are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="13948-106">Sin embargo, se deben volver a compilar los archivos binarios de versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="13948-106">However, binaries from earlier versions of Windows must be recompiled.</span></span>

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a><span data-ttu-id="13948-107">Trasladar aplicaciones de copia de seguridad de Windows XP a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13948-107">Porting Windows XP Backup Applications to Windows Vista</span></span>

<span data-ttu-id="13948-108">Varias interfaces VSS han cambiado desde Windows XP.</span><span class="sxs-lookup"><span data-stu-id="13948-108">Several VSS interfaces have changed since Windows XP.</span></span> <span data-ttu-id="13948-109">Como mínimo, las aplicaciones de Windows XP se deben volver a compilar mediante archivos de encabezado y bibliotecas del SDK de VSS 7,2 o el SDK de Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="13948-109">At a minimum, Windows XP applications must be recompiled using header files and libraries from the VSS 7.2 SDK or the Windows Vista or Windows Server 2008 SDK.</span></span>

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a><span data-ttu-id="13948-110">Trasladar aplicaciones de copia de seguridad de Windows Server 2003 SP1 a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13948-110">Porting Windows Server 2003 SP1 Backup Applications to Windows Vista</span></span>

<span data-ttu-id="13948-111">Los archivos binarios de Windows Server 2003 con SP1 son compatibles con Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="13948-111">Binaries from Windows Server 2003 with SP1 are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="13948-112">Sin embargo, la mayoría de las aplicaciones de copia de seguridad de Windows Server 2003 con SP1 se deben actualizar para tener en cuenta las nuevas características, que se describen en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="13948-112">However, most Windows Server 2003 with SP1 backup applications must be updated to account for new features, which are described in the following sections.</span></span>

## <a name="compiling-backup-applications-for-windows-vista"></a><span data-ttu-id="13948-113">Compilar aplicaciones de copia de seguridad para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13948-113">Compiling Backup Applications for Windows Vista</span></span>

<span data-ttu-id="13948-114">Las aplicaciones que usan interfaces disponibles en Windows Server 2003 se pueden compilar mediante archivos de encabezado y bibliotecas proporcionadas en el SDK de VSS 7,2.</span><span class="sxs-lookup"><span data-stu-id="13948-114">Applications that use interfaces available in Windows Server 2003 can be compiled using header files and libraries provided in the VSS 7.2 SDK.</span></span> <span data-ttu-id="13948-115">Para usar nuevas interfaces, las aplicaciones se deben volver a compilar con los archivos de encabezado y las bibliotecas incluidas en el SDK de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13948-115">To use new interfaces, applications must be recompiled using the header files and libraries included in the Windows Vista SDK.</span></span>

> [!Note]  
> <span data-ttu-id="13948-116">Los archivos binarios compilados con Windows Vista o Windows Server 2008 no son compatibles con Windows Server 2003 con SP1 o versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="13948-116">Binaries compiled using Windows Vista or Windows Server 2008 are not compatible with Windows Server 2003 with SP1 or earlier versions of Windows.</span></span>

 

 

 



