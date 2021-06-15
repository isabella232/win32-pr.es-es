---
title: Tipos de enumeración de cliente DRM de Microsoft Windows Media
description: Obtenga información sobre las enumeraciones que son compatibles con las API extendidas del cliente DRM de Microsoft Windows Media.
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- Windows Media Format SDK,tipos de enumeración
- administración de derechos digitales (DRM), tipos de enumeración
- DRM (administración de derechos digitales), tipos de enumeración
- API extendidas de cliente DRM, tipos de enumeración
- API extendidas de cliente, tipos de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574136f8016161f4d2c208865a72ad2a86d98f68
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068432"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="172ea-108">Tipos de enumeración de cliente DRM de Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="172ea-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="172ea-109">En la tabla siguiente se describen las enumeraciones que son compatibles con las API extendidas del cliente DRM de Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="172ea-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="172ea-110">Enumeración</span><span class="sxs-lookup"><span data-stu-id="172ea-110">Enumeration</span></span>                                                                      | <span data-ttu-id="172ea-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="172ea-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="172ea-112">**ACCIÓN DRM \_ \_ PERMITIDOS \_ RESULTADOS DE \_ CONSULTA**</span><span class="sxs-lookup"><span data-stu-id="172ea-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="172ea-113">Usado por [**la interfaz IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) para especificar el motivo por el que no se permite una acción.</span><span class="sxs-lookup"><span data-stu-id="172ea-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="172ea-114">**TIPO \_ DE DATOS ATTR DE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="172ea-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="172ea-115">Define los tipos de datos usados para los atributos y propiedades de DRM.</span><span class="sxs-lookup"><span data-stu-id="172ea-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="172ea-116">**TIPO \_ DE CRIPTOGRAFÍA \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="172ea-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="172ea-117">Define los tipos de algoritmos criptográficos que se pueden usar para cifrar el contenido.</span><span class="sxs-lookup"><span data-stu-id="172ea-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="172ea-118">**ESTADO \_ HTTP DE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="172ea-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="172ea-119">Define un intervalo de estados HTTP para una solicitud DRM.</span><span class="sxs-lookup"><span data-stu-id="172ea-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="172ea-120">**ESTADO \_ DE INDIVIDUALIZACIÓN DE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="172ea-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="172ea-121">Define los estados válidos para la individualización de DRM.</span><span class="sxs-lookup"><span data-stu-id="172ea-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="172ea-122">**CATEGORÍA ESTADO \_ DE \_ LICENCIA \_ DE DRM**</span><span class="sxs-lookup"><span data-stu-id="172ea-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="172ea-123">Especifica el tipo de restricción de licencia que se describe en una estructura [**\_ DRM LICENSE STATE \_ \_ DATA.**](drmdrm-license-state-data.md)</span><span class="sxs-lookup"><span data-stu-id="172ea-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="172ea-124">**ESTADO DE \_ MSDRM**</span><span class="sxs-lookup"><span data-stu-id="172ea-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="172ea-125">Define las condiciones de estado para el subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="172ea-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="172ea-126">**TIPO DE DIRECTIVA \_ \_ WMDRMNET**</span><span class="sxs-lookup"><span data-stu-id="172ea-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="172ea-127">Enumera los tipos de directivas que están disponibles para DRM de Windows Media para las operaciones de dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="172ea-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="172ea-128">**DERECHOS \_ DE WMT**</span><span class="sxs-lookup"><span data-stu-id="172ea-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="172ea-129">Define los derechos que se pueden especificar en una licencia DRM.</span><span class="sxs-lookup"><span data-stu-id="172ea-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="172ea-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="172ea-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="172ea-131">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="172ea-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




