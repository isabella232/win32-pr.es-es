---
description: Define métodos para obtener información acerca de las propiedades de un elemento de búsqueda. Esta interfaz solo se admite en Windows XP y Windows Server 2003 y ya no debe usarse.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Interfaz IItemPropertyBag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153939"
---
# <a name="iitempropertybag-interface"></a><span data-ttu-id="69bbb-104">Interfaz IItemPropertyBag</span><span class="sxs-lookup"><span data-stu-id="69bbb-104">IItemPropertyBag interface</span></span>

<span data-ttu-id="69bbb-105">Define métodos para obtener información acerca de las propiedades de un elemento de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="69bbb-105">Defines methods to obtain information about the properties of a search item.</span></span> <span data-ttu-id="69bbb-106">Esta interfaz solo se admite en Windows XP y Windows Server 2003 y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="69bbb-106">This interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="69bbb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="69bbb-107">Members</span></span>

<span data-ttu-id="69bbb-108">La interfaz **IItemPropertyBag** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="69bbb-108">The **IItemPropertyBag** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="69bbb-109">**IItemPropertyBag** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="69bbb-109">**IItemPropertyBag** also has these types of members:</span></span>

-   [<span data-ttu-id="69bbb-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="69bbb-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="69bbb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="69bbb-111">Methods</span></span>

<span data-ttu-id="69bbb-112">La interfaz **IItemPropertyBag** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="69bbb-112">The **IItemPropertyBag** interface has these methods.</span></span>



| <span data-ttu-id="69bbb-113">Método</span><span class="sxs-lookup"><span data-stu-id="69bbb-113">Method</span></span>                                                      | <span data-ttu-id="69bbb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="69bbb-114">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="69bbb-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="69bbb-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span></span> | <span data-ttu-id="69bbb-116">Obtiene un recuento del número de propiedades del contenedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="69bbb-116">Gets a count of the number of properties in the property bag.</span></span><br/>                     |
| [<span data-ttu-id="69bbb-117">**GetPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="69bbb-117">**GetPropertyInfo**</span></span>](iitempropertybag-getpropertyinfo.md) | <span data-ttu-id="69bbb-118">Obtiene la información necesaria para leer o guardar las propiedades en el contenedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="69bbb-118">Gets the information required to read or save the properties in the property bag.</span></span><br/> |
| [<span data-ttu-id="69bbb-119">**Lectura**</span><span class="sxs-lookup"><span data-stu-id="69bbb-119">**Read**</span></span>](iitempropertybag-read.md)                       | <span data-ttu-id="69bbb-120">Hace que una o más propiedades se lean del contenedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="69bbb-120">Causes one or more properties to be read from the property bag.</span></span><br/>                   |
| [<span data-ttu-id="69bbb-121">**Escritura**</span><span class="sxs-lookup"><span data-stu-id="69bbb-121">**Write**</span></span>](iitempropertybag-write.md)                     | <span data-ttu-id="69bbb-122">Hace que una o más propiedades se guarden en el contenedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="69bbb-122">Causes one or more properties to be saved into the property bag.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="69bbb-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69bbb-123">Remarks</span></span>

<span data-ttu-id="69bbb-124">La interfaz **IItemPropertyBag** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="69bbb-124">The **IItemPropertyBag** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="69bbb-125">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz **IItemPropertyBag** y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) y [**ISearchItem**](-search-isearchitem.md) , las estructuras [**LINKINFO**](-search-linkinfo.md) y [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="69bbb-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPropertyBag** interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="69bbb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69bbb-126">Requirements</span></span>



| <span data-ttu-id="69bbb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="69bbb-127">Requirement</span></span> | <span data-ttu-id="69bbb-128">Value</span><span class="sxs-lookup"><span data-stu-id="69bbb-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="69bbb-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69bbb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="69bbb-130">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="69bbb-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="69bbb-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69bbb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="69bbb-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="69bbb-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="69bbb-133">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="69bbb-133">Redistributable</span></span><br/>          | <span data-ttu-id="69bbb-134">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="69bbb-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
