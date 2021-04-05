---
title: Editar atributos de metadatos
description: Editar atributos de metadatos
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- SDK de Windows Media Format, Editar atributos de metadatos
- Advanced Systems Format (ASF), Editar atributos de metadatos
- ASF (formato de sistemas avanzados), Editar atributos de metadatos
- metadatos, Editar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420314"
---
# <a name="editing-metadata-attributes"></a><span data-ttu-id="8b92b-107">Editar atributos de metadatos</span><span class="sxs-lookup"><span data-stu-id="8b92b-107">Editing Metadata Attributes</span></span>

<span data-ttu-id="8b92b-108">La edición de atributos de metadatos es muy similar a la configuración de otras nuevas.</span><span class="sxs-lookup"><span data-stu-id="8b92b-108">Editing metadata attributes is very similar to setting new ones.</span></span> <span data-ttu-id="8b92b-109">En lugar de usar [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), use [**IWMHeaderInfo3:: ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute).</span><span class="sxs-lookup"><span data-stu-id="8b92b-109">Instead of using [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), use [**IWMHeaderInfo3::ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute).</span></span> <span data-ttu-id="8b92b-110">**ModifyAttribute** es idéntico a **AddAttribute** , salvo que no se especifica un nombre de atributo y el número de índice es un parámetro de entrada en lugar de un resultado.</span><span class="sxs-lookup"><span data-stu-id="8b92b-110">**ModifyAttribute** is identical to **AddAttribute** except that you do not specify an attribute name, and the index number is an input parameter instead of an output.</span></span>

<span data-ttu-id="8b92b-111">Puede usar el número de secuencia 0xFFFF para especificar un atributo que se va a modificar mediante su índice global.</span><span class="sxs-lookup"><span data-stu-id="8b92b-111">You can use stream number 0xFFFF to specify an attribute to modify using its global index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b92b-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b92b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b92b-113">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="8b92b-113">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




