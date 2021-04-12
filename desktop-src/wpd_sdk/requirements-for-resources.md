---
description: Requisitos para recursos
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Requisitos para recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277995"
---
# <a name="requirements-for-resources"></a><span data-ttu-id="a77f5-103">Requisitos para recursos</span><span class="sxs-lookup"><span data-stu-id="a77f5-103">Requirements for Resources</span></span>

<span data-ttu-id="a77f5-104">Dispositivos portátiles de Windows define las siguientes categorías de recursos como valores de **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="a77f5-104">Windows Portable Devices defines the following resource categories as **PROPERTYKEY** values.</span></span> <span data-ttu-id="a77f5-105">Estos valores se usan para describir los recursos individuales de un objeto.</span><span class="sxs-lookup"><span data-stu-id="a77f5-105">These values are used to describe individual resources in an object.</span></span> <span data-ttu-id="a77f5-106">El miembro *PID* de la clave de propiedad puede ser diferente para describir los distintos recursos del mismo tipo para todos los tipos, excepto el **\_ \_ valor predeterminado del recurso WPD**, que solo puede describir un recurso.</span><span class="sxs-lookup"><span data-stu-id="a77f5-106">The *pid* member of the property key can be different to describe different resources of the same type for all types except **WPD\_RESOURCE\_DEFAULT**, which can only describe one resource.</span></span> <span data-ttu-id="a77f5-107">En la página Descripción vinculada de cada tipo de recurso se enumeran los atributos admitidos por ese recurso.</span><span class="sxs-lookup"><span data-stu-id="a77f5-107">The linked description page for each resource type lists the attributes supported by that resource.</span></span>



| <span data-ttu-id="a77f5-108">PROPERTYKEY de recursos</span><span class="sxs-lookup"><span data-stu-id="a77f5-108">Resource PROPERTYKEY</span></span>                                                | <span data-ttu-id="a77f5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a77f5-109">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a77f5-110">**\_valor predeterminado del recurso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a77f5-110">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md)              | <span data-ttu-id="a77f5-111">Especifica el archivo completo detrás del objeto.</span><span class="sxs-lookup"><span data-stu-id="a77f5-111">Specifies the whole file behind the object.</span></span> <span data-ttu-id="a77f5-112">Este es el único recurso necesario para cualquier objeto con un recurso.</span><span class="sxs-lookup"><span data-stu-id="a77f5-112">This is the only required resource for any object with a resource.</span></span> |
| [<span data-ttu-id="a77f5-113">**\_carátula de \_ álbum de recursos de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a77f5-113">**WPD\_RESOURCE\_ALBUM\_ART**</span></span>](wpd-resource-album-art.md)         | <span data-ttu-id="a77f5-114">Especifica una imagen que representa la ilustración del álbum para el objeto.</span><span class="sxs-lookup"><span data-stu-id="a77f5-114">Specifies an image that represents the album artwork for the object.</span></span>                                           |
| [<span data-ttu-id="a77f5-115">**\_clip de \_ audio de recursos de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a77f5-115">**WPD\_RESOURCE\_AUDIO\_CLIP**</span></span>](wpd-resource-audio-clip.md)       | <span data-ttu-id="a77f5-116">Especifica un clip de audio para el objeto.</span><span class="sxs-lookup"><span data-stu-id="a77f5-116">Specifies an audio clip for the object.</span></span>                                                                        |
| [<span data-ttu-id="a77f5-117">**\_foto de \_ contacto de recursos de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a77f5-117">**WPD\_RESOURCE\_CONTACT\_PHOTO**</span></span>](wpd-resource-contact-photo.md) | <span data-ttu-id="a77f5-118">Especifica una imagen que representa una fotografía de la persona a la que se hace referencia en el objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="a77f5-118">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>                |
| [<span data-ttu-id="a77f5-119">**\_recursos genéricos del recurso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a77f5-119">**WPD\_RESOURCE\_GENERIC**</span></span>](wpd-resource-generic.md)              | <span data-ttu-id="a77f5-120">Un recurso genérico de tipo de datos undefined.</span><span class="sxs-lookup"><span data-stu-id="a77f5-120">A generic resource of undefined data type.</span></span> <span data-ttu-id="a77f5-121">Esto se debe tratar como una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="a77f5-121">This should be treated as a byte array.</span></span>                             |
| [<span data-ttu-id="a77f5-122">**\_icono de recurso de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a77f5-122">**WPD\_RESOURCE\_ICON**</span></span>](wpd-resource-icon.md)                    | <span data-ttu-id="a77f5-123">Un icono.</span><span class="sxs-lookup"><span data-stu-id="a77f5-123">An icon.</span></span>                                                                                                       |
| [<span data-ttu-id="a77f5-124">**\_miniatura de recursos de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a77f5-124">**WPD\_RESOURCE\_THUMBNAIL**</span></span>](wpd-resource-thumbnail.md)          | <span data-ttu-id="a77f5-125">Imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="a77f5-125">A thumbnail image.</span></span>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="a77f5-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a77f5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a77f5-127">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="a77f5-127">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



