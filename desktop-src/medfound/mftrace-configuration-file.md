---
description: La herramienta MFTrace puede leer un archivo de configuración XML que especifica uno o más proveedores de seguimiento.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: Archivo de configuración MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6598bcfdde16291fb744783b2f12be414ae997b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652551"
---
# <a name="mftrace-configuration-file"></a><span data-ttu-id="66cfa-103">Archivo de configuración MFTrace</span><span class="sxs-lookup"><span data-stu-id="66cfa-103">MFTrace Configuration File</span></span>

<span data-ttu-id="66cfa-104">La herramienta [MFTrace](mftrace.md) puede leer un archivo de configuración XML que especifica uno o más proveedores de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="66cfa-104">The [MFTrace](mftrace.md) tool can read an XML configuration file that specifies one or more trace providers.</span></span>

<span data-ttu-id="66cfa-105">El elemento [**providers**](providers.md) es el elemento raíz del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="66cfa-105">The [**providers**](providers.md) element is the root element in the configuration file.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="66cfa-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="66cfa-106">In this section</span></span>

-   [<span data-ttu-id="66cfa-107">**palabra clave**</span><span class="sxs-lookup"><span data-stu-id="66cfa-107">**keyword**</span></span>](keyword.md)
-   [<span data-ttu-id="66cfa-108">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="66cfa-108">**mfdetours**</span></span>](mfdetours.md)
-   [<span data-ttu-id="66cfa-109">**presta**</span><span class="sxs-lookup"><span data-stu-id="66cfa-109">**provider**</span></span>](provider.md)
-   [<span data-ttu-id="66cfa-110">**providers**</span><span class="sxs-lookup"><span data-stu-id="66cfa-110">**providers**</span></span>](providers.md)

## <a name="example"></a><span data-ttu-id="66cfa-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66cfa-111">Example</span></span>

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a><span data-ttu-id="66cfa-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66cfa-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66cfa-113">MFTrace</span><span class="sxs-lookup"><span data-stu-id="66cfa-113">MFTrace</span></span>](mftrace.md)
</dt> </dl>

 

 



