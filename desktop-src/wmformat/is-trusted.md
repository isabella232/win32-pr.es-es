---
title: Is_Trusted
description: El \_ atributo is Trusted es un atributo de nivel de archivo que especifica si la dirección URL de adquisición de licencias en el archivo es de confianza.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted formato de Windows Media
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994776"
---
# <a name="is_trusted"></a><span data-ttu-id="dc783-104">Es de \_ confianza</span><span class="sxs-lookup"><span data-stu-id="dc783-104">Is\_Trusted</span></span>

<span data-ttu-id="dc783-105">El atributo **is \_ Trusted** es un atributo de nivel de archivo que especifica si la dirección URL de adquisición de licencias en el archivo es de confianza.</span><span class="sxs-lookup"><span data-stu-id="dc783-105">The **Is\_Trusted** attribute is a file-level attribute specifying whether the license acquisition URL in the file is trusted.</span></span>

## <a name="global-constant"></a><span data-ttu-id="dc783-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="dc783-106">Global Constant</span></span>

<span data-ttu-id="dc783-107">g \_ wszWMTrusted</span><span class="sxs-lookup"><span data-stu-id="dc783-107">g\_wszWMTrusted</span></span>

## <a name="data-type"></a><span data-ttu-id="dc783-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="dc783-108">Data Type</span></span>

<span data-ttu-id="dc783-109">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="dc783-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="dc783-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc783-110">Remarks</span></span>

<span data-ttu-id="dc783-111">Se trata de un atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="dc783-111">This is a coded attribute.</span></span>

<span data-ttu-id="dc783-112">Antes de navegar a una dirección URL de adquisición de licencias incluida en un archivo protegido con DRM, una aplicación debe comprobar primero si esta propiedad es true.</span><span class="sxs-lookup"><span data-stu-id="dc783-112">Before navigating to a license acquisition URL contained in a DRM-protected file, an application should first verify that this property is true.</span></span> <span data-ttu-id="dc783-113">Si es false, la aplicación debe notificar al usuario que es posible que la dirección URL se haya alterado.</span><span class="sxs-lookup"><span data-stu-id="dc783-113">If it is false, the application should notify the user that the URL has possibly been tampered with.</span></span>

<span data-ttu-id="dc783-114">Este atributo no se puede duplicar en el nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="dc783-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="dc783-115">Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="dc783-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc783-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc783-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc783-117">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="dc783-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




