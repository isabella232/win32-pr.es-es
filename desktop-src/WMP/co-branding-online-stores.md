---
title: Co-Branding tiendas en línea
description: Co-Branding tiendas en línea
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player tiendas en línea, personalización de marca
- tiendas en línea, personalización de marca
- tipo 1 tiendas en línea, personalización de marca
- tipo 2 tiendas en línea, personalización de marca
- tiendas en línea con personalización de marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695310"
---
# <a name="co-branding-online-stores"></a><span data-ttu-id="fa303-108">Co-Branding tiendas en línea</span><span class="sxs-lookup"><span data-stu-id="fa303-108">Co-Branding Online Stores</span></span>

<span data-ttu-id="fa303-109">Los OEM de equipos personales que no operan una tienda de música pueden coexistir con proveedores de tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="fa303-109">Personal computer OEMs who do not operate a music store can co-brand with online store providers.</span></span> <span data-ttu-id="fa303-110">El programa de instalación de Windows Media Player admite el parámetro de línea de comandos ServiceExtra para permitir que los OEM de hardware establezcan un atributo personalizado que la tienda en línea pueda usar para identificar qué OEM instaló la tienda en línea inicial.</span><span class="sxs-lookup"><span data-stu-id="fa303-110">Windows Media Player setup supports the ServiceExtra command line parameter to enable hardware OEMs to set a custom attribute that the online store can use to identify which OEM installed the initial online store.</span></span>

<span data-ttu-id="fa303-111">Por ejemplo, si un creador de equipo llamado Fabrikam desea establecer la tienda en línea inicial en el almacén de música de Proseware, podría usar la siguiente línea de comandos para instalar Windows Media Player 10:</span><span class="sxs-lookup"><span data-stu-id="fa303-111">For example, if a computer maker named Fabrikam wants to set the initial online store to the Proseware music store, it might use the following command line to install Windows Media Player 10:</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



<span data-ttu-id="fa303-112">Cuando Windows Media Player se instala de esta manera, el reproductor anexa la cadena ServiceExtra cada vez que abre el servicio Proseware.</span><span class="sxs-lookup"><span data-stu-id="fa303-112">When Windows Media Player is installed in this manner, the Player appends the ServiceExtra string each time it opens the Proseware service.</span></span> <span data-ttu-id="fa303-113">En el ejemplo siguiente se muestra la dirección URL que Windows Media Player enviará al servicio Proseware para recuperar el documento ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="fa303-113">The following example shows the URL that Windows Media Player would send to the Proseware service to retrieve the ServiceInfo document:</span></span>


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



<span data-ttu-id="fa303-114">La tienda en línea de Proseware puede usar la cadena de consulta para determinar qué OEM instaló Windows Media Player y devolver un documento de ServiceInfo generado dinámicamente que apunte a la versión con personalización de marca de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="fa303-114">The Proseware online store can then use the query string to determine which OEM installed Windows Media Player and return a dynamically generated ServiceInfo document that points to the co-branded version of the online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa303-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fa303-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa303-116">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="fa303-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="fa303-117">**Parámetros de la línea de comandos del programa de instalación para tiendas en línea**</span><span class="sxs-lookup"><span data-stu-id="fa303-117">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




