---
description: Proporciona métodos para proporcionar la configuración del explorador. La interfaz IItemPreviewerExt solo se admite en Windows XP y Windows Server 2003, y ya no debe usarse.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Interfaz IItemPreviewerExt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000996"
---
# <a name="iitempreviewerext-interface"></a><span data-ttu-id="1f407-104">Interfaz IItemPreviewerExt</span><span class="sxs-lookup"><span data-stu-id="1f407-104">IItemPreviewerExt interface</span></span>

<span data-ttu-id="1f407-105">Proporciona métodos para proporcionar la configuración del explorador.</span><span class="sxs-lookup"><span data-stu-id="1f407-105">Provides methods for supplying browser settings.</span></span> <span data-ttu-id="1f407-106">La interfaz **IItemPreviewerExt** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="1f407-106">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="1f407-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1f407-107">Members</span></span>

<span data-ttu-id="1f407-108">La interfaz **IItemPreviewerExt** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1f407-108">The **IItemPreviewerExt** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1f407-109">**IItemPreviewerExt** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1f407-109">**IItemPreviewerExt** also has these types of members:</span></span>

-   [<span data-ttu-id="1f407-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f407-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1f407-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f407-111">Methods</span></span>

<span data-ttu-id="1f407-112">La interfaz **IItemPreviewerExt** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1f407-112">The **IItemPreviewerExt** interface has these methods.</span></span>



| <span data-ttu-id="1f407-113">Método</span><span class="sxs-lookup"><span data-stu-id="1f407-113">Method</span></span>                                                                               | <span data-ttu-id="1f407-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f407-114">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f407-115">**GetLinkedContent**</span><span class="sxs-lookup"><span data-stu-id="1f407-115">**GetLinkedContent**</span></span>](-search-iitempreviewerext-getlinkedcontent.md)               | <span data-ttu-id="1f407-116">Permite la extensión a contenido enriquecido para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="1f407-116">Permits the extension to rich content for a property.</span></span> <br/>                            |
| [<span data-ttu-id="1f407-117">**GetRelatedPart**</span><span class="sxs-lookup"><span data-stu-id="1f407-117">**GetRelatedPart**</span></span>](-search-iitempreviewerext-getrelatedpart.md)                   | <span data-ttu-id="1f407-118">Obtiene una parte del cuerpo relacionada para la inserción en el flujo MHTML de salida.</span><span class="sxs-lookup"><span data-stu-id="1f407-118">Gets a related body part for embedding into the output MHTML stream.</span></span><br/>              |
| [<span data-ttu-id="1f407-119">**ProcessTransformCommand**</span><span class="sxs-lookup"><span data-stu-id="1f407-119">**ProcessTransformCommand**</span></span>](-search-iitempreviewerext-processtransformcommand.md) | <span data-ttu-id="1f407-120">Permite el procesamiento de un comando de transformación que se encuentra en una plantilla de vista previa.</span><span class="sxs-lookup"><span data-stu-id="1f407-120">Permits processing of a transformation command encountered in a preview template.</span></span><br/> |
| [<span data-ttu-id="1f407-121">**SuggestBrowserPolicy**</span><span class="sxs-lookup"><span data-stu-id="1f407-121">**SuggestBrowserPolicy**</span></span>](-search-iitempreviewerext-suggestbrowserpolicy.md)       | <span data-ttu-id="1f407-122">Sugiere la Directiva de seguridad que se va a aplicar al explorador.</span><span class="sxs-lookup"><span data-stu-id="1f407-122">Suggests the security policy to be applied to the browser.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="1f407-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f407-123">Remarks</span></span>

<span data-ttu-id="1f407-124">La interfaz **IItemPreviewerExt** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="1f407-124">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="1f407-125">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz **IItemPreviewerExt** y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="1f407-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPreviewerExt** interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f407-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f407-126">Requirements</span></span>



| <span data-ttu-id="1f407-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f407-127">Requirement</span></span> | <span data-ttu-id="1f407-128">Value</span><span class="sxs-lookup"><span data-stu-id="1f407-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f407-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f407-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1f407-130">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f407-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1f407-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f407-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1f407-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f407-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1f407-133">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1f407-133">Redistributable</span></span><br/>          | <span data-ttu-id="1f407-134">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="1f407-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
