---
description: La propiedad Resumen de palabras clave de las bases de datos de instalación o transformaciones contiene una lista de palabras clave.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Propiedad de Resumen de palabras clave
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690668"
---
# <a name="keywords-summary-property"></a><span data-ttu-id="72a5c-103">Propiedad de Resumen de palabras clave</span><span class="sxs-lookup"><span data-stu-id="72a5c-103">Keywords Summary property</span></span>

<span data-ttu-id="72a5c-104">La propiedad **Resumen de palabras clave** de las bases de datos de instalación o transformaciones contiene una lista de palabras clave.</span><span class="sxs-lookup"><span data-stu-id="72a5c-104">The **Keywords Summary** property in installation databases or transforms contains a list of keywords.</span></span> <span data-ttu-id="72a5c-105">Los exploradores de archivos pueden usar las palabras clave para realizar búsquedas de palabras clave para un archivo.</span><span class="sxs-lookup"><span data-stu-id="72a5c-105">The keywords may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="72a5c-106">Esta propiedad contiene una lista de orígenes de la revisión en un paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="72a5c-106">This property contains a list of sources of the patch in a patch package.</span></span>

<span data-ttu-id="72a5c-107">Es el autor de una base de datos de instalación, una transformación o un paquete de revisión que proporcione el valor de esta propiedad en la información de resumen.</span><span class="sxs-lookup"><span data-stu-id="72a5c-107">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="72a5c-108">Los autores deben hacer lo siguiente para determinar el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="72a5c-108">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="72a5c-109">En un paquete de instalación, establezca el valor de esta propiedad en una lista de palabras clave.</span><span class="sxs-lookup"><span data-stu-id="72a5c-109">In an installation package, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="72a5c-110">La palabra clave debe incluir "Installer", así como palabras clave específicas del producto, y se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="72a5c-110">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="72a5c-111">En una transformación, establezca el valor de esta propiedad en una lista de palabras clave.</span><span class="sxs-lookup"><span data-stu-id="72a5c-111">In a transform, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="72a5c-112">La palabra clave debe incluir "Installer", así como palabras clave específicas del producto, y se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="72a5c-112">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="72a5c-113">En un paquete de revisión, establezca el valor de esta propiedad en una lista delimitada por signos de punto y coma de ubicaciones de red o direcciones URL para los orígenes de la revisión.</span><span class="sxs-lookup"><span data-stu-id="72a5c-113">In a patch package, set the value of this property to a semicolon-delimited list of network or URL locations for the sources of the patch.</span></span> <span data-ttu-id="72a5c-114">Cuando se instala la revisión, el instalador las agrega a la lista de origen del paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="72a5c-114">When the patch is installed, the installer adds these to the source list for the patch package.</span></span> <span data-ttu-id="72a5c-115">Si falta la revisión almacenada en caché, el instalador puede buscar un origen en la ubicación original, una ubicación agregada a la lista de origen mediante la propiedad de **Resumen palabras clave** o una ubicación agregada a la lista de origen mediante las funciones [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) o [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) .</span><span class="sxs-lookup"><span data-stu-id="72a5c-115">If the cached patch becomes missing, the installer can search for a source in the original location, a location added to the source list by the **Keywords Summary** property, or a location added to the source list using the [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) or [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="72a5c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72a5c-116">Requirements</span></span>



| <span data-ttu-id="72a5c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="72a5c-117">Requirement</span></span> | <span data-ttu-id="72a5c-118">Value</span><span class="sxs-lookup"><span data-stu-id="72a5c-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72a5c-119">Versión</span><span class="sxs-lookup"><span data-stu-id="72a5c-119">Version</span></span><br/> | <span data-ttu-id="72a5c-120">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="72a5c-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="72a5c-121">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="72a5c-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="72a5c-122">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="72a5c-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72a5c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="72a5c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72a5c-124">Descripciones de propiedades de Resumen</span><span class="sxs-lookup"><span data-stu-id="72a5c-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




