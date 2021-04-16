---
description: Proporciona un método para invocar objetos ISearchItem.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Interfaz ISearchProtocolUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705491"
---
# <a name="isearchprotocolui-interface"></a><span data-ttu-id="a642d-103">Interfaz ISearchProtocolUI</span><span class="sxs-lookup"><span data-stu-id="a642d-103">ISearchProtocolUI interface</span></span>

<span data-ttu-id="a642d-104">Proporciona un método para invocar objetos [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a642d-104">Provides a method for invoking [**ISearchItem**](-search-isearchitem.md) objects.</span></span> <span data-ttu-id="a642d-105">El host del protocolo llama a los métodos de esta interfaz al procesar las direcciones URL del recopilador.</span><span class="sxs-lookup"><span data-stu-id="a642d-105">Methods in this interface are called by the protocol host when processing URLs from the gatherer.</span></span> <span data-ttu-id="a642d-106">El controlador de protocolo implementa el protocolo para tener acceso a un origen de contenido en su formato nativo y esta interfaz implementa un controlador de protocolo personalizado para expandir los orígenes de datos que se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="a642d-106">The protocol handler implements the protocol for accessing a content source in its native format, and this interface implements a custom protocol handler to expand the data sources that can be indexed.</span></span>

## <a name="members"></a><span data-ttu-id="a642d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a642d-107">Members</span></span>

<span data-ttu-id="a642d-108">La interfaz **ISearchProtocolUI** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a642d-108">The **ISearchProtocolUI** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a642d-109">**ISearchProtocolUI** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a642d-109">**ISearchProtocolUI** also has these types of members:</span></span>

-   [<span data-ttu-id="a642d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a642d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a642d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a642d-111">Methods</span></span>

<span data-ttu-id="a642d-112">La interfaz **ISearchProtocolUI** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a642d-112">The **ISearchProtocolUI** interface has these methods.</span></span>



| <span data-ttu-id="a642d-113">Método</span><span class="sxs-lookup"><span data-stu-id="a642d-113">Method</span></span>                                                                       | <span data-ttu-id="a642d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a642d-114">Description</span></span>                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a642d-115">**GetSearchItemForUrl**</span><span class="sxs-lookup"><span data-stu-id="a642d-115">**GetSearchItemForUrl**</span></span>](-search-isearchprotocolui-getsearchitemforurl.md) | <span data-ttu-id="a642d-116">Obtiene el elemento de búsqueda para los datos especificados.</span><span class="sxs-lookup"><span data-stu-id="a642d-116">Gets the search item for the data specified.</span></span> <span data-ttu-id="a642d-117">Se llama a este método una vez por cada dirección URL procesada por el recopilador y recupera un puntero al objeto [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a642d-117">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="a642d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a642d-118">Remarks</span></span>

<span data-ttu-id="a642d-119">La interfaz **ISearchProtocolUI** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="a642d-119">The **ISearchProtocolUI** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="a642d-120">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz **ISearchProtocolUI** y las siguientes API: las interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="a642d-120">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchProtocolUI** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a642d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a642d-121">Requirements</span></span>



| <span data-ttu-id="a642d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a642d-122">Requirement</span></span> | <span data-ttu-id="a642d-123">Value</span><span class="sxs-lookup"><span data-stu-id="a642d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a642d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a642d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a642d-125">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a642d-125">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a642d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a642d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a642d-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a642d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a642d-128">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a642d-128">Redistributable</span></span><br/>          | <span data-ttu-id="a642d-129">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="a642d-129">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
