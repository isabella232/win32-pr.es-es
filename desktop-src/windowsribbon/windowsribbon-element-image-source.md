---
title: Image. Source (propiedad)
description: Representa la ruta de acceso al directorio de una imagen.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Imagen. Source (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801898"
---
# <a name="imagesource-property"></a><span data-ttu-id="f36ed-104">Image. Source (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f36ed-104">Image.Source property</span></span>

<span data-ttu-id="f36ed-105">Representa la ruta de acceso al directorio de una imagen.</span><span class="sxs-lookup"><span data-stu-id="f36ed-105">Represents the directory path of an image.</span></span>

## <a name="usage"></a><span data-ttu-id="f36ed-106">Uso</span><span class="sxs-lookup"><span data-stu-id="f36ed-106">Usage</span></span>

``` syntax
<Image.Source/>
```

## <a name="attributes"></a><span data-ttu-id="f36ed-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="f36ed-107">Attributes</span></span>

<span data-ttu-id="f36ed-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="f36ed-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f36ed-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f36ed-109">Child elements</span></span>

<span data-ttu-id="f36ed-110">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="f36ed-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f36ed-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="f36ed-111">Parent elements</span></span>



| <span data-ttu-id="f36ed-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="f36ed-112">Element</span></span>                                                 |
|---------------------------------------------------------|
| [<span data-ttu-id="f36ed-113">**Impresión**</span><span class="sxs-lookup"><span data-stu-id="f36ed-113">**Image**</span></span>](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f36ed-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f36ed-114">Remarks</span></span>

<span data-ttu-id="f36ed-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f36ed-115">Optional.</span></span>

<span data-ttu-id="f36ed-116">Puede producirse al menos una vez para cada [**imagen**](windowsribbon-element-image.md).</span><span class="sxs-lookup"><span data-stu-id="f36ed-116">May occur at most once for each [**Image**](windowsribbon-element-image.md).</span></span>

<span data-ttu-id="f36ed-117">Este elemento contiene un valor de tipo *xs: anyURI* o cualquier secuencia de caracteres que representa un identificador uniforme de recursos (URI).</span><span class="sxs-lookup"><span data-stu-id="f36ed-117">This element contains a value of type *xs:anyURI* or any sequence of characters that represents a Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="f36ed-118">El valor del URI es una ruta de acceso absoluta o relativa (en el archivo de marcado de la cinta de opciones) del directorio de un recurso de imagen de tipo Bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="f36ed-118">The URI value is an absolute or relative (to the Ribbon markup file) directory path of an image resource of type bitmap (BMP).</span></span>

## <a name="examples"></a><span data-ttu-id="f36ed-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f36ed-119">Examples</span></span>

<span data-ttu-id="f36ed-120">En el ejemplo de código siguiente se muestra el marcado necesario para declarar, a través de un conjunto de elementos de [**imagen**](windowsribbon-element-image.md) , una colección de recursos de imagen que están diseñados para admitir cuatro configuraciones de PPP de pantalla específicas.</span><span class="sxs-lookup"><span data-stu-id="f36ed-120">The following code example shows the markup required to declare, through a set of [**Image**](windowsribbon-element-image.md) elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span> <span data-ttu-id="f36ed-121">La propiedad **Image. Source** se usa para especificar la ruta de acceso al recurso de imagen.</span><span class="sxs-lookup"><span data-stu-id="f36ed-121">The **Image.Source** property is used to specify the path to the image resource.</span></span>


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="f36ed-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f36ed-122">Requirements</span></span>



| <span data-ttu-id="f36ed-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f36ed-123">Requirement</span></span> | <span data-ttu-id="f36ed-124">Value</span><span class="sxs-lookup"><span data-stu-id="f36ed-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f36ed-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f36ed-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f36ed-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f36ed-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f36ed-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f36ed-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f36ed-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f36ed-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





