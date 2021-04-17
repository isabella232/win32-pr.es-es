---
description: 'Los valores del registro de WFP se encuentran en la siguiente clave del registro: HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Valores del registro de WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668441"
---
# <a name="wfp-registry-values"></a><span data-ttu-id="21e7e-103">Valores del registro de WFP</span><span class="sxs-lookup"><span data-stu-id="21e7e-103">WFP Registry Values</span></span>

<span data-ttu-id="21e7e-104">\[Los valores del registro de WFP no se admiten en Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="21e7e-104">\[WFP registry values are not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="21e7e-105">WFP usa varios valores del registro para la configuración de personalización.</span><span class="sxs-lookup"><span data-stu-id="21e7e-105">WFP uses several registry values for customization settings.</span></span> <span data-ttu-id="21e7e-106">Los valores del registro de WFP se encuentran en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="21e7e-106">The WFP registry values are located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

<span data-ttu-id="21e7e-107">Estos son los valores del registro de WFP.</span><span class="sxs-lookup"><span data-stu-id="21e7e-107">The following are the WFP registry values.</span></span>

<dl> <dt>

<span data-ttu-id="21e7e-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span><span class="sxs-lookup"><span data-stu-id="21e7e-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span></span>
</dt> <dd>

<span data-ttu-id="21e7e-109">Ubicación de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="21e7e-109">Location of the cache.</span></span> <span data-ttu-id="21e7e-110">Debe ser una ruta de acceso local.</span><span class="sxs-lookup"><span data-stu-id="21e7e-110">This must be a local path.</span></span> <span data-ttu-id="21e7e-111">El valor predeterminado es% SystemRoot% \\ system32 \\ dllcache.</span><span class="sxs-lookup"><span data-stu-id="21e7e-111">The default value is %systemroot%\\system32\\dllcache.</span></span>

</dd> <dt>

<span data-ttu-id="21e7e-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span><span class="sxs-lookup"><span data-stu-id="21e7e-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span></span>
</dt> <dd>

<span data-ttu-id="21e7e-113">Opciones de cuota.</span><span class="sxs-lookup"><span data-stu-id="21e7e-113">Quota options.</span></span> <span data-ttu-id="21e7e-114">Este valor del registro puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="21e7e-114">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="21e7e-115">Value</span><span class="sxs-lookup"><span data-stu-id="21e7e-115">Value</span></span>                  | <span data-ttu-id="21e7e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="21e7e-116">Meaning</span></span>                                                  |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="21e7e-117">\_ \_ todos \_ los archivos de cuota de SFC</span><span class="sxs-lookup"><span data-stu-id="21e7e-117">SFC\_QUOTA\_ALL\_FILES</span></span> | <span data-ttu-id="21e7e-118">El tamaño de la caché de DLL es ilimitado.</span><span class="sxs-lookup"><span data-stu-id="21e7e-118">Size of the DLL cache is unlimited.</span></span> <span data-ttu-id="21e7e-119">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="21e7e-119">This is the default.</span></span> |
| <span data-ttu-id="21e7e-120">Otros valores</span><span class="sxs-lookup"><span data-stu-id="21e7e-120">Other values</span></span>           | <span data-ttu-id="21e7e-121">Tamaño de la caché de DLL, en archivos.</span><span class="sxs-lookup"><span data-stu-id="21e7e-121">Size of the DLL cache, in files.</span></span>                         |



 

</dd> <dt>

<span data-ttu-id="21e7e-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span><span class="sxs-lookup"><span data-stu-id="21e7e-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span></span>
</dt> <dd>

<span data-ttu-id="21e7e-123">Opciones de examen.</span><span class="sxs-lookup"><span data-stu-id="21e7e-123">Scan options.</span></span> <span data-ttu-id="21e7e-124">Este valor del registro puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="21e7e-124">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="21e7e-125">Value</span><span class="sxs-lookup"><span data-stu-id="21e7e-125">Value</span></span>             | <span data-ttu-id="21e7e-126">Significado</span><span class="sxs-lookup"><span data-stu-id="21e7e-126">Meaning</span></span>                                                   |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="21e7e-127">examen de SFC \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="21e7e-127">SFC\_SCAN\_NORMAL</span></span> | <span data-ttu-id="21e7e-128">No examinar archivos protegidos en el arranque.</span><span class="sxs-lookup"><span data-stu-id="21e7e-128">Do not scan protected files at boot.</span></span> <span data-ttu-id="21e7e-129">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="21e7e-129">This is the default.</span></span> |
| <span data-ttu-id="21e7e-130">detección de SFC \_ \_ siempre</span><span class="sxs-lookup"><span data-stu-id="21e7e-130">SFC\_SCAN\_ALWAYS</span></span> | <span data-ttu-id="21e7e-131">Examinar los archivos protegidos en cada arranque.</span><span class="sxs-lookup"><span data-stu-id="21e7e-131">Scan protected files at every boot.</span></span>                       |
| <span data-ttu-id="21e7e-132">\_examinar SFC \_ una vez</span><span class="sxs-lookup"><span data-stu-id="21e7e-132">SFC\_SCAN\_ONCE</span></span>   | <span data-ttu-id="21e7e-133">Examinar los archivos protegidos en el siguiente arranque.</span><span class="sxs-lookup"><span data-stu-id="21e7e-133">Scan protected files at the next boot.</span></span>                    |



 

</dd> </dl>

 

 



