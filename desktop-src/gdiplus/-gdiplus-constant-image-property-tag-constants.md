---
description: Varios formatos de archivo de imagen permiten almacenar metadatos junto con una imagen.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Constantes de etiqueta de propiedad de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985203"
---
# <a name="image-property-tag-constants"></a><span data-ttu-id="950b5-103">Constantes de etiqueta de propiedad de imagen</span><span class="sxs-lookup"><span data-stu-id="950b5-103">Image Property Tag Constants</span></span>

<span data-ttu-id="950b5-104">Varios formatos de archivo de imagen permiten almacenar metadatos junto con una imagen.</span><span class="sxs-lookup"><span data-stu-id="950b5-104">Several image file formats enable you to store metadata along with an image.</span></span> <span data-ttu-id="950b5-105">Los metadatos son información acerca de una imagen, como el título, el ancho, el modelo de cámara y el artista.</span><span class="sxs-lookup"><span data-stu-id="950b5-105">Metadata is information about an image, for example, title, width, camera model, and artist.</span></span> <span data-ttu-id="950b5-106">Windows GDI+ proporciona una manera uniforme de almacenar y recuperar metadatos de archivos de imagen en los formatos de Tagged Image File Format (TIFF), JPEG, gráficos de red portátiles (PNG) y de archivo de imagen intercambiable (EXIF).</span><span class="sxs-lookup"><span data-stu-id="950b5-106">Windows GDI+ provides a uniform way of storing and retrieving metadata from image files in the Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG), and Exchangeable Image File (EXIF) formats.</span></span>

<span data-ttu-id="950b5-107">En GDI+, una parte de los metadatos se denomina *elemento de propiedad* y un elemento de propiedad individual se identifica mediante una constante numérica denominada etiqueta de *propiedad*.</span><span class="sxs-lookup"><span data-stu-id="950b5-107">In GDI+, a piece of metadata is called a *property item*, and an individual property item is identified by a numerical constant called a *property tag*.</span></span> <span data-ttu-id="950b5-108">Puede almacenar y recuperar los metadatos mediante una llamada a los métodos [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) e [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) de la clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , y no tiene que preocuparse por los detalles de cómo un formato de archivo determinado almacena esos metadatos.</span><span class="sxs-lookup"><span data-stu-id="950b5-108">You can store and retrieve metadata by calling the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) and [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned with the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="950b5-109">En los temas siguientes se enumeran y describen los elementos de propiedad admitidos por GDI+.</span><span class="sxs-lookup"><span data-stu-id="950b5-109">The following topics list and describe the property items supported by GDI+.</span></span> <span data-ttu-id="950b5-110">Las descripciones son breves y generales para que se apliquen a una variedad de formatos de archivo.</span><span class="sxs-lookup"><span data-stu-id="950b5-110">The descriptions are brief and general so that they apply to a variety of file formats.</span></span> <span data-ttu-id="950b5-111">Para obtener una descripción detallada de cómo se usa un elemento de propiedad en un formato de archivo determinado, vea la especificación de ese formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="950b5-111">For a detailed description of how a property item is used in a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="950b5-112">Para obtener vínculos a varias especificaciones de formato de archivo, consulte [Especificaciones de formato de archivo de imagen](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="950b5-112">For links to several file format specifications, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span> <span data-ttu-id="950b5-113">Para obtener más información sobre los metadatos, vea [lectura y escritura de metadatos](-gdiplus-reading-and-writing-metadata-use.md) y [**constantes de tipo de etiqueta de propiedad de imagen**](-gdiplus-constant-image-property-tag-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="950b5-113">For more information about metadata, see [Reading and Writing Metadata](-gdiplus-reading-and-writing-metadata-use.md) and [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span>

-   [<span data-ttu-id="950b5-114">Etiquetas de propiedad en orden numérico</span><span class="sxs-lookup"><span data-stu-id="950b5-114">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [<span data-ttu-id="950b5-115">Etiquetas de propiedad en orden alfabético</span><span class="sxs-lookup"><span data-stu-id="950b5-115">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [<span data-ttu-id="950b5-116">Descripciones de elementos de propiedad</span><span class="sxs-lookup"><span data-stu-id="950b5-116">Property Item Descriptions</span></span>](-gdiplus-constant-property-item-descriptions.md)

 

 



