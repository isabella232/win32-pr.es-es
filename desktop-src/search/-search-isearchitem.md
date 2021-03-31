---
description: Proporciona métodos que definen la interacción entre una interfaz de usuario (UI) y los objetos de espacio de nombres de búsqueda creados por el indizador.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Interfaz ISearchItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423731"
---
# <a name="isearchitem-interface"></a><span data-ttu-id="39d87-103">Interfaz ISearchItem</span><span class="sxs-lookup"><span data-stu-id="39d87-103">ISearchItem interface</span></span>

<span data-ttu-id="39d87-104">Proporciona métodos que definen la interacción entre una interfaz de usuario (UI) y los objetos de espacio de nombres de búsqueda creados por el indizador.</span><span class="sxs-lookup"><span data-stu-id="39d87-104">Provides methods that define interaction between a user interface (UI) and the Search namespace objects created by the indexer.</span></span>

## <a name="members"></a><span data-ttu-id="39d87-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="39d87-105">Members</span></span>

<span data-ttu-id="39d87-106">La interfaz **ISearchItem** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="39d87-106">The **ISearchItem** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="39d87-107">**ISearchItem** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="39d87-107">**ISearchItem** also has these types of members:</span></span>

-   [<span data-ttu-id="39d87-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="39d87-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="39d87-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="39d87-109">Methods</span></span>

<span data-ttu-id="39d87-110">La interfaz **ISearchItem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="39d87-110">The **ISearchItem** interface has these methods.</span></span>



| <span data-ttu-id="39d87-111">Método</span><span class="sxs-lookup"><span data-stu-id="39d87-111">Method</span></span>                                                         | <span data-ttu-id="39d87-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="39d87-112">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39d87-113">**GetParentFolder**</span><span class="sxs-lookup"><span data-stu-id="39d87-113">**GetParentFolder**</span></span>](-search-isearchitem-getparentfolder.md) | <span data-ttu-id="39d87-114">Obtiene el objeto **ISearchItem** si la dirección URL representa un origen de datos de Shell real (también conocido como una extensión de espacio de nombres de Shell).</span><span class="sxs-lookup"><span data-stu-id="39d87-114">Gets the **ISearchItem** object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span><br/> |
| <span data-ttu-id="39d87-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39d87-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span></span>     | <span data-ttu-id="39d87-116">Obtiene el objeto de interfaz de usuario (UI) de **ISearchItem**.</span><span class="sxs-lookup"><span data-stu-id="39d87-116">Gets the user interface (UI) object of **ISearchItem**.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="39d87-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39d87-117">Remarks</span></span>

<span data-ttu-id="39d87-118">[**ISearchItem:: GetParentFolder**](-search-isearchitem-getparentfolder.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="39d87-118">The [**ISearchItem::GetParentFolder**](-search-isearchitem-getparentfolder.md) is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="39d87-119">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz **ISearchItem** y las siguientes API: las interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)y [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="39d87-119">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchItem** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d87-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39d87-120">Requirements</span></span>



| <span data-ttu-id="39d87-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="39d87-121">Requirement</span></span> | <span data-ttu-id="39d87-122">Value</span><span class="sxs-lookup"><span data-stu-id="39d87-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39d87-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39d87-123">Minimum supported client</span></span><br/> | <span data-ttu-id="39d87-124">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="39d87-124">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="39d87-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39d87-125">Minimum supported server</span></span><br/> | <span data-ttu-id="39d87-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="39d87-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="39d87-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="39d87-127">Redistributable</span></span><br/>          | <span data-ttu-id="39d87-128">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="39d87-128">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
