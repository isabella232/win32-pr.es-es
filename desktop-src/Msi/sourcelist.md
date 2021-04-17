---
description: La propiedad SOURCELIST es una lista delimitada por signos de punto y coma de rutas de acceso de origen de red o URL al paquete de instalación de la aplicación.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: Propiedad SOURCELIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653369"
---
# <a name="sourcelist-property"></a><span data-ttu-id="efea5-103">Propiedad SOURCELIST</span><span class="sxs-lookup"><span data-stu-id="efea5-103">SOURCELIST property</span></span>

<span data-ttu-id="efea5-104">La propiedad **SourceList** es una lista delimitada por signos de punto y coma de rutas de acceso de origen de red o URL al paquete de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="efea5-104">The **SOURCELIST** property is a semicolon-delimited list of network or URL source paths to the application's installation package.</span></span> <span data-ttu-id="efea5-105">Esta lista se anexa al final de la lista de origen existente de cada usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="efea5-105">This list is appended to the end of each user's existing source list for the application.</span></span> <span data-ttu-id="efea5-106">El instalador busca un origen enumerando la lista de rutas de acceso de origen y utiliza la primera ubicación accesible que encuentra.</span><span class="sxs-lookup"><span data-stu-id="efea5-106">The installer locates a source by enumerating the list of source paths and uses the first accessible location it finds.</span></span> <span data-ttu-id="efea5-107">Solo se puede usar este origen para el resto de la instalación.</span><span class="sxs-lookup"><span data-stu-id="efea5-107">Only this source can be used for the remainder of the installation.</span></span> <span data-ttu-id="efea5-108">Por lo tanto, cada ruta de acceso especificada en la lista de origen debe ser a una ubicación que tenga un origen completo para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="efea5-108">Each path specified in the source list must therefore be to a location having a complete source for the application.</span></span> <span data-ttu-id="efea5-109">Todo el árbol de directorios en cada ubicación de origen debe ser el mismo y debe incluir todos los archivos de origen necesarios, incluidos los contenedores.</span><span class="sxs-lookup"><span data-stu-id="efea5-109">The entire directory tree at each source location must be the same and must include all of the required source files, including any cabinets.</span></span> <span data-ttu-id="efea5-110">Cada ubicación debe tener un archivo. msi con el mismo nombre de archivo y el mismo código de producto.</span><span class="sxs-lookup"><span data-stu-id="efea5-110">Each location must have an .msi file with the same file name and product code.</span></span>

## <a name="default-value"></a><span data-ttu-id="efea5-111">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="efea5-111">Default Value</span></span>

<span data-ttu-id="efea5-112">El instalador solo comprueba la propiedad **SourceList** si el producto aún no se ha anunciado o instalado.</span><span class="sxs-lookup"><span data-stu-id="efea5-112">The installer only checks the **SOURCELIST** property if the product has not already been advertised or installed.</span></span> <span data-ttu-id="efea5-113">En todos los demás casos, el instalador usa la lista de orígenes existente que se encuentra en el registro.</span><span class="sxs-lookup"><span data-stu-id="efea5-113">In all other cases the installer uses the existing source list that is in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="efea5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efea5-114">Remarks</span></span>

<span data-ttu-id="efea5-115">Los orígenes agregados mediante la propiedad **SourceList** se agregan directamente al final de la lista para cada tipo de origen y siempre van después del origen predeterminado especificado por la propiedad [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="efea5-115">Sources added using the **SOURCELIST** property are added directly to the end of the list for each type of source and always come after the default source specified by the [**SourceDir**](sourcedir.md) property.</span></span>

<span data-ttu-id="efea5-116">Por Windows Installer el número de orígenes de la propiedad **SourceList** es ilimitado.</span><span class="sxs-lookup"><span data-stu-id="efea5-116">For Windows Installer the number of sources in the **SOURCELIST** property is unlimited.</span></span> <span data-ttu-id="efea5-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) se puede usar para agregar orígenes de red.</span><span class="sxs-lookup"><span data-stu-id="efea5-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) can be used to add network sources.</span></span>

## <a name="requirements"></a><span data-ttu-id="efea5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efea5-118">Requirements</span></span>



| <span data-ttu-id="efea5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="efea5-119">Requirement</span></span> | <span data-ttu-id="efea5-120">Value</span><span class="sxs-lookup"><span data-stu-id="efea5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efea5-121">Versión</span><span class="sxs-lookup"><span data-stu-id="efea5-121">Version</span></span><br/> | <span data-ttu-id="efea5-122">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="efea5-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="efea5-123">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="efea5-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="efea5-124">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="efea5-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="efea5-125">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="efea5-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efea5-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="efea5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efea5-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="efea5-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="efea5-128">Resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="efea5-128">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




