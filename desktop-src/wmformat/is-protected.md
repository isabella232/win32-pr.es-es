---
title: Is_Protected
description: El \_ atributo is Protected es un atributo de nivel de archivo que especifica si el contenido del archivo se protegió mediante la administración de derechos digitales (DRM).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected formato de Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105714325"
---
# <a name="is_protected"></a><span data-ttu-id="25404-104">Está \_ protegido</span><span class="sxs-lookup"><span data-stu-id="25404-104">Is\_Protected</span></span>

<span data-ttu-id="25404-105">El atributo **is \_ Protected** es un atributo de nivel de archivo que especifica si el contenido del archivo se protegió mediante la administración de derechos digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="25404-105">The **Is\_Protected** attribute is a file-level attribute specifying whether the content in the file was protected using digital rights management (DRM).</span></span>

## <a name="global-constant"></a><span data-ttu-id="25404-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="25404-106">Global Constant</span></span>

<span data-ttu-id="25404-107">g \_ wszWMProtected</span><span class="sxs-lookup"><span data-stu-id="25404-107">g\_wszWMProtected</span></span>

## <a name="data-type"></a><span data-ttu-id="25404-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="25404-108">Data Type</span></span>

<span data-ttu-id="25404-109">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="25404-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="25404-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25404-110">Remarks</span></span>

<span data-ttu-id="25404-111">Se trata de un atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="25404-111">This is a coded attribute.</span></span> <span data-ttu-id="25404-112">La recuperación de esta propiedad proporciona la misma información que llamar a [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span><span class="sxs-lookup"><span data-stu-id="25404-112">Retrieving this property provides the same information as calling [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span></span>

<span data-ttu-id="25404-113">Este atributo no se puede duplicar en el nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="25404-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="25404-114">Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="25404-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="25404-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="25404-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25404-116">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="25404-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




