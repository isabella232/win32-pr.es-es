---
title: HasAttachedImages
description: El atributo HasAttachedImages es un atributo de nivel de archivo que especifica si el archivo es un archivo MP3 con tramas ID3 de APIC conectadas.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- HasAttachedImages formato de Windows Media
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695542"
---
# <a name="hasattachedimages"></a><span data-ttu-id="a7760-104">HasAttachedImages</span><span class="sxs-lookup"><span data-stu-id="a7760-104">HasAttachedImages</span></span>

<span data-ttu-id="a7760-105">El atributo **HasAttachedImages** es un atributo de nivel de archivo que especifica si el archivo es un archivo MP3 con tramas ID3 de APIC conectadas.</span><span class="sxs-lookup"><span data-stu-id="a7760-105">The **HasAttachedImages** attribute is a file-level attribute specifying whether the file is an MP3 file with attached APIC ID3 frames.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a7760-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="a7760-106">Global Constant</span></span>

<span data-ttu-id="a7760-107">g \_ wszWMHasAttachedImages</span><span class="sxs-lookup"><span data-stu-id="a7760-107">g\_wszWMHasAttachedImages</span></span>

## <a name="data-type"></a><span data-ttu-id="a7760-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a7760-108">Data Type</span></span>

<span data-ttu-id="a7760-109">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a7760-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="a7760-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7760-110">Remarks</span></span>

<span data-ttu-id="a7760-111">Se trata de un atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="a7760-111">This is a coded attribute.</span></span>

<span data-ttu-id="a7760-112">Este atributo no se puede duplicar en el nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="a7760-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="a7760-113">Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="a7760-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="a7760-114">**HasAttachedImages** se diseñó para informar a una aplicación de que las imágenes estaban presentes para que se pudieran recuperar mediante la interfaz [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) .</span><span class="sxs-lookup"><span data-stu-id="a7760-114">**HasAttachedImages** was designed to inform an application that images were present so that they could be retrieved using the [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) interface.</span></span> <span data-ttu-id="a7760-115">Ahora que se admiten las imágenes mediante el atributo [**WM/imagen**](wmpicture.md) , **HasAttachedImages** ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="a7760-115">Now that images are supported using the [**WM/Picture**](wmpicture.md) attribute, **HasAttachedImages** is no longer needed.</span></span>

<span data-ttu-id="a7760-116">Para determinar si un archivo contiene imágenes, llame a [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) especificando el atributo **WM/imagen** .</span><span class="sxs-lookup"><span data-stu-id="a7760-116">To determine whether a file contains images, call [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) specifying the **WM/Picture** attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7760-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7760-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7760-118">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="a7760-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




