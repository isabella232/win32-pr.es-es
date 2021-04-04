---
title: Tipos de enumeración de cliente DRM de Microsoft Windows Media
description: Tipos de enumeración
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- SDK de Windows Media Format, tipos de enumeración
- Administración de derechos digitales (DRM), tipos de enumeración
- DRM (administración de derechos digitales), tipos de enumeración
- API extendidas del cliente DRM, tipos de enumeración
- API extendidas de cliente, tipos de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159342367035767d213d57987d93d23eb321a6c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078733"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="7152a-108">Tipos de enumeración de cliente DRM de Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="7152a-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="7152a-109">En la tabla siguiente se describen las enumeraciones admitidas por las API extendidas del cliente DRM de Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7152a-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="7152a-110">Enumeración</span><span class="sxs-lookup"><span data-stu-id="7152a-110">Enumeration</span></span>                                                                      | <span data-ttu-id="7152a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7152a-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7152a-112">**la \_ acción \_ DRM \_ permitió \_ resultados de la consulta**</span><span class="sxs-lookup"><span data-stu-id="7152a-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="7152a-113">Lo usa la interfaz [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) para especificar la razón por la que no se permite una acción.</span><span class="sxs-lookup"><span data-stu-id="7152a-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="7152a-114">**TIPO de los atributos de DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7152a-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="7152a-115">Define los tipos de datos utilizados para los atributos y propiedades de DRM.</span><span class="sxs-lookup"><span data-stu-id="7152a-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="7152a-116">**\_tipo criptográfico de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7152a-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="7152a-117">Define los tipos de algoritmos criptográficos que se pueden usar para cifrar el contenido.</span><span class="sxs-lookup"><span data-stu-id="7152a-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="7152a-118">**\_Estado http de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7152a-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="7152a-119">Define un intervalo de Estados HTTP para una solicitud DRM.</span><span class="sxs-lookup"><span data-stu-id="7152a-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="7152a-120">**\_Estado de individualización de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7152a-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="7152a-121">Define los Estados válidos para la individualización de DRM.</span><span class="sxs-lookup"><span data-stu-id="7152a-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="7152a-122">**\_categoría de \_ Estado de licencia de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7152a-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="7152a-123">Especifica el tipo de restricción de licencia que se describe mediante una estructura de [**datos de estado de licencia de DRM \_ \_ \_**](drmdrm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="7152a-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="7152a-124">**Estado de MSDRM \_**</span><span class="sxs-lookup"><span data-stu-id="7152a-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="7152a-125">Define las condiciones de estado para el subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="7152a-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="7152a-126">**\_tipo de directiva WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="7152a-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="7152a-127">Enumera los tipos de directivas que están disponibles para las operaciones de Windows Media DRM para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="7152a-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="7152a-128">**derechos de WMT \_**</span><span class="sxs-lookup"><span data-stu-id="7152a-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="7152a-129">Define los derechos que se pueden especificar en una licencia de DRM.</span><span class="sxs-lookup"><span data-stu-id="7152a-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="7152a-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7152a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7152a-131">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="7152a-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




