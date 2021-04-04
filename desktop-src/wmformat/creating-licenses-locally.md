---
title: Crear licencias localmente
description: Crear licencias localmente
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- SDK de Windows Media Format, crear licencias localmente
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), creación de licencias localmente
- DRM (administración de derechos digitales), crear licencias localmente
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas del cliente DRM, creación de licencias localmente
- API extendidas del cliente, crear licencias localmente
- licencias, crear licencias localmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fc4305c77be2132611df925ae08458fe2bb4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076341"
---
# <a name="creating-licenses-locally"></a><span data-ttu-id="12705-112">Crear licencias localmente</span><span class="sxs-lookup"><span data-stu-id="12705-112">Creating Licenses Locally</span></span>

<span data-ttu-id="12705-113">En determinadas circunstancias, como durante la [importación de DRM](drm-import.md), puede crear sus propias licencias.</span><span class="sxs-lookup"><span data-stu-id="12705-113">In certain circumstances, such as during [DRM Import](drm-import.md), you can create your own licenses.</span></span> <span data-ttu-id="12705-114">Las licencias de DRM de Windows Media se pueden escribir de varias maneras diferentes, pero para crear su propia licencia debe usar el esquema binario de derechos de multimedia extensible (XMR).</span><span class="sxs-lookup"><span data-stu-id="12705-114">Windows Media DRM licenses can be written a few different ways, but to make your own license, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="12705-115">Para obtener más información, consulte [Building a XMR License](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="12705-115">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>

<span data-ttu-id="12705-116">Al crear una licencia, puede agregarla al almacén de licencias local llamando al método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="12705-116">When you create a license, you can add it to the local license store by calling the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12705-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12705-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12705-118">**Adquisición de licencias**</span><span class="sxs-lookup"><span data-stu-id="12705-118">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="12705-119">**Creación de una licencia de XMR**</span><span class="sxs-lookup"><span data-stu-id="12705-119">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> </dl>

 

 




