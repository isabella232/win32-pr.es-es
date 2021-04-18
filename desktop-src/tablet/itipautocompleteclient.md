---
description: Permite al cliente llamar al objeto de proveedor de finalización automática del panel de entrada de texto de la aplicación.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interfaz ITipAutocompleteClient (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717069"
---
# <a name="itipautocompleteclient-interface"></a><span data-ttu-id="3d0d3-103">Interfaz ITipAutocompleteClient</span><span class="sxs-lookup"><span data-stu-id="3d0d3-103">ITipAutocompleteClient interface</span></span>

<span data-ttu-id="3d0d3-104">Permite al cliente llamar al objeto de proveedor de finalización automática del panel de entrada de texto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d0d3-104">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span>

## <a name="members"></a><span data-ttu-id="3d0d3-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="3d0d3-105">Members</span></span>

<span data-ttu-id="3d0d3-106">La interfaz **ITipAutocompleteClient** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3d0d3-106">The **ITipAutocompleteClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3d0d3-107">**ITipAutocompleteClient** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3d0d3-107">**ITipAutocompleteClient** also has these types of members:</span></span>

-   [<span data-ttu-id="3d0d3-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3d0d3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3d0d3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="3d0d3-109">Methods</span></span>

<span data-ttu-id="3d0d3-110">La interfaz **ITipAutocompleteClient** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3d0d3-110">The **ITipAutocompleteClient** interface has these methods.</span></span>



| <span data-ttu-id="3d0d3-111">Método</span><span class="sxs-lookup"><span data-stu-id="3d0d3-111">Method</span></span>                                                              | <span data-ttu-id="3d0d3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d0d3-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d0d3-113">**AdviseProvider**</span><span class="sxs-lookup"><span data-stu-id="3d0d3-113">**AdviseProvider**</span></span>](itipautocompleteclient-adviseprovider.md)     | <span data-ttu-id="3d0d3-114">Registra el proveedor con el cliente para permitir que el cliente llame al objeto de proveedor de autocompletar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d0d3-114">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="3d0d3-115">**PreferredRects**</span><span class="sxs-lookup"><span data-stu-id="3d0d3-115">**PreferredRects**</span></span>](itipautocompleteclient-preferredrects.md)     | <span data-ttu-id="3d0d3-116">Permite al cliente sugerir dónde colocar la lista de Autocompletar para evitar la superposición del panel de entrada.</span><span class="sxs-lookup"><span data-stu-id="3d0d3-116">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span><br/>                                               |
| [<span data-ttu-id="3d0d3-117">**RequestShowUI**</span><span class="sxs-lookup"><span data-stu-id="3d0d3-117">**RequestShowUI**</span></span>](itipautocompleteclient-requestshowui.md)       | <span data-ttu-id="3d0d3-118">Determina si el panel de entrada está listo para mostrar la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="3d0d3-118">Determines whether Input Panel is ready to have the auto complete list shown.</span></span><br/>                                                                             |
| [<span data-ttu-id="3d0d3-119">**UnadviseProvider**</span><span class="sxs-lookup"><span data-stu-id="3d0d3-119">**UnadviseProvider**</span></span>](itipautocompleteclient-unadviseprovider.md) | <span data-ttu-id="3d0d3-120">Anula el registro del proveedor asociado.</span><span class="sxs-lookup"><span data-stu-id="3d0d3-120">Unregisters the associated provider.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="3d0d3-121">**UserSelection**</span><span class="sxs-lookup"><span data-stu-id="3d0d3-121">**UserSelection**</span></span>](itipautocompleteclient-userselection.md)       | <span data-ttu-id="3d0d3-122">Notifica al panel de entrada que el usuario ha seleccionado algo en la lista de autocompletar y descartar todo el texto restante que todavía no se ha insertado.</span><span class="sxs-lookup"><span data-stu-id="3d0d3-122">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3d0d3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d0d3-123">Requirements</span></span>



| <span data-ttu-id="3d0d3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d0d3-124">Requirement</span></span> | <span data-ttu-id="3d0d3-125">Value</span><span class="sxs-lookup"><span data-stu-id="3d0d3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d0d3-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d0d3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3d0d3-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3d0d3-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="3d0d3-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d0d3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3d0d3-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3d0d3-129">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="3d0d3-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d0d3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d0d3-131"><dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3d0d3-131"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3d0d3-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d0d3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d0d3-133"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d0d3-133"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



 

