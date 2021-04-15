---
description: Si esta Directiva del sistema por equipo se establece en un valor mayor que 0, Windows Installer guarda las versiones anteriores de los archivos en una memoria caché cuando se aplica una revisión a una aplicación.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497699"
---
# <a name="maxpatchcachesize"></a><span data-ttu-id="ab4b2-103">MaxPatchCacheSize</span><span class="sxs-lookup"><span data-stu-id="ab4b2-103">MaxPatchCacheSize</span></span>

<span data-ttu-id="ab4b2-104">Si esta [Directiva del sistema](system-policy.md) por equipo se establece en un valor mayor que 0, Windows Installer guarda las versiones anteriores de los archivos en una memoria caché cuando se aplica una revisión a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab4b2-104">If this per-machine [system policy](system-policy.md) is set to a value greater than 0, Windows Installer saves older versions of files in a cache when a patch is applied to an application.</span></span> <span data-ttu-id="ab4b2-105">El almacenamiento en caché puede aumentar el rendimiento de las instalaciones futuras que, de otro modo, necesitan obtener los archivos antiguos de un origen de aplicación original.</span><span class="sxs-lookup"><span data-stu-id="ab4b2-105">Caching can increase the performance of future installations that otherwise need to obtain the old files from a original application source.</span></span>

<span data-ttu-id="ab4b2-106">El valor de la Directiva MaxPatchCacheSize es el porcentaje máximo de espacio en disco que puede usar el instalador para la caché de archivos antiguos.</span><span class="sxs-lookup"><span data-stu-id="ab4b2-106">The value of the MaxPatchCacheSize policy is the maximum percentage of disk space that the installer can use for the cache of old files.</span></span> <span data-ttu-id="ab4b2-107">Por ejemplo, un valor de 20 no especifica más del 20%.</span><span class="sxs-lookup"><span data-stu-id="ab4b2-107">For example, a value of 20 specifies no more than 20% be used.</span></span> <span data-ttu-id="ab4b2-108">Si el tamaño total de la memoria caché alcanza el porcentaje especificado de espacio en disco, no se guarda ningún archivo adicional en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="ab4b2-108">If the total size of the cache reaches the specified percentage of disk space, no additional files are saved to the cache.</span></span> <span data-ttu-id="ab4b2-109">La Directiva no afecta a los archivos que ya se han guardado.</span><span class="sxs-lookup"><span data-stu-id="ab4b2-109">The policy does not affect files that have already been saved.</span></span>

<span data-ttu-id="ab4b2-110">Si el valor de la Directiva MaxPatchCacheSize se establece en 0, no se guarda ningún archivo adicional.</span><span class="sxs-lookup"><span data-stu-id="ab4b2-110">If the value of the MaxPatchCacheSize policy is set to 0, no additional files are saved.</span></span>

<span data-ttu-id="ab4b2-111">Si no se establece la Directiva MaxPatchCacheSize, el valor predeterminado es 10 y se puede usar un máximo del 10% del espacio en disco para guardar los archivos antiguos.</span><span class="sxs-lookup"><span data-stu-id="ab4b2-111">If the MaxPatchCacheSize policy is not set, the default value is 10 and a maximum of 10% of the disk space can be used to save old files.</span></span>

## <a name="registry-key"></a><span data-ttu-id="ab4b2-112">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="ab4b2-112">Registry Key</span></span>

<span data-ttu-id="ab4b2-113">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="ab4b2-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="ab4b2-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ab4b2-114">Data Type</span></span>

<span data-ttu-id="ab4b2-115">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="ab4b2-115">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab4b2-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab4b2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab4b2-117">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="ab4b2-117">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



