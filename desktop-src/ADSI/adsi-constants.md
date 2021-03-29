---
title: Constantes ADSI
description: En la tabla siguiente se enumeran las constantes definidas y utilizadas en Active Directory interfaces de servicio (ADSI).
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773021"
---
# <a name="adsi-constants"></a><span data-ttu-id="ec19a-109">Constantes ADSI</span><span class="sxs-lookup"><span data-stu-id="ec19a-109">ADSI Constants</span></span>

<span data-ttu-id="ec19a-110">En la tabla siguiente se enumeran las constantes definidas y utilizadas en Active Directory interfaces de servicio (ADSI).</span><span class="sxs-lookup"><span data-stu-id="ec19a-110">The following table lists constants defined and used in Active Directory Service Interfaces (ADSI).</span></span>



| <span data-ttu-id="ec19a-111">ADSI (constante)</span><span class="sxs-lookup"><span data-stu-id="ec19a-111">ADSI constant</span></span>                      | <span data-ttu-id="ec19a-112">Value</span><span class="sxs-lookup"><span data-stu-id="ec19a-112">Value</span></span>                                   | <span data-ttu-id="ec19a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec19a-113">Description</span></span>                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec19a-114">**INITCREDENTIALS de ADS \_ ext \_**</span><span class="sxs-lookup"><span data-stu-id="ec19a-114">**ADS\_EXT\_INITCREDENTIALS**</span></span>      | <span data-ttu-id="ec19a-115">1</span><span class="sxs-lookup"><span data-stu-id="ec19a-115">1</span></span>                                       | <span data-ttu-id="ec19a-116">Código de control que indica que los datos personalizados proporcionados al método [**IADsExtension:: Operating**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contienen las credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="ec19a-116">A control code that indicates that the custom data supplied to the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method contains user credentials.</span></span>                                                     |
| <span data-ttu-id="ec19a-117">**\_ \_ finalización de la inicialización de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="ec19a-117">**ADS\_EXT\_INITIALIZE\_COMPLETE**</span></span> | <span data-ttu-id="ec19a-118">2</span><span class="sxs-lookup"><span data-stu-id="ec19a-118">2</span></span>                                       | <span data-ttu-id="ec19a-119">Código de control que se usa con [**IADsExtension:: Operating**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) para indicar que las extensiones pueden realizar cualquier inicialización necesaria, en función de las características admitidas por el objeto primario.</span><span class="sxs-lookup"><span data-stu-id="ec19a-119">A control code used with [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) to indicate that extensions can perform any necessary initialization, depending on the features supported by the parent object.</span></span> |
| <span data-ttu-id="ec19a-120">**MAXEXTDISPID de ADS \_ ext \_**</span><span class="sxs-lookup"><span data-stu-id="ec19a-120">**ADS\_EXT\_MAXEXTDISPID**</span></span>         | <span data-ttu-id="ec19a-121">16777215</span><span class="sxs-lookup"><span data-stu-id="ec19a-121">16777215</span></span>                                | <span data-ttu-id="ec19a-122">El DISPID más alto que un objeto de extensión puede usar para sus métodos y propiedades.</span><span class="sxs-lookup"><span data-stu-id="ec19a-122">The highest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                   |
| <span data-ttu-id="ec19a-123">**MINEXTDISPID de ADS \_ ext \_**</span><span class="sxs-lookup"><span data-stu-id="ec19a-123">**ADS\_EXT\_MINEXTDISPID**</span></span>         | <span data-ttu-id="ec19a-124">1</span><span class="sxs-lookup"><span data-stu-id="ec19a-124">1</span></span>                                       | <span data-ttu-id="ec19a-125">El DISPID más bajo que un objeto de extensión puede usar para sus métodos y propiedades.</span><span class="sxs-lookup"><span data-stu-id="ec19a-125">The lowest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                    |
| <span data-ttu-id="ec19a-126">**\_respuesta VLV de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="ec19a-126">**ADS\_VLV\_RESPONSE**</span></span>             | <span data-ttu-id="ec19a-127">L "fc8cb04d-311D-406c-8cb9-1ae8b843b419"</span><span class="sxs-lookup"><span data-stu-id="ec19a-127">L"fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span></span> | <span data-ttu-id="ec19a-128">Se usa con el método [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para recuperar los metadatos de búsqueda VLV.</span><span class="sxs-lookup"><span data-stu-id="ec19a-128">Used with the [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) method to retrieve VLV search metadata.</span></span> <span data-ttu-id="ec19a-129">Para obtener más información, consulte [Cómo buscar con VLV](how-to-search-using-vlv.md).</span><span class="sxs-lookup"><span data-stu-id="ec19a-129">For more information, see [How to Search Using VLV](how-to-search-using-vlv.md).</span></span>        |
| <span data-ttu-id="ec19a-130">**DBPROPFLAGS \_ ADSISEARCH**</span><span class="sxs-lookup"><span data-stu-id="ec19a-130">**DBPROPFLAGS\_ADSISEARCH**</span></span>        | <span data-ttu-id="ec19a-131">0x0000C000</span><span class="sxs-lookup"><span data-stu-id="ec19a-131">0x0000C000</span></span>                              | <span data-ttu-id="ec19a-132">Se utiliza para trabajar con el proveedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="ec19a-132">Used to work with the OLE DB provider.</span></span>                                                                                                                                                                           |



 

 

 




