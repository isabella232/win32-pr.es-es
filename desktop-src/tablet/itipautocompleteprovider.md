---
description: Administra el lado de la aplicación de la integración de autocompletar del panel de entrada de texto.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Interfaz ITipAutocompleteProvider (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717155"
---
# <a name="itipautocompleteprovider-interface"></a><span data-ttu-id="061a4-103">Interfaz ITipAutocompleteProvider</span><span class="sxs-lookup"><span data-stu-id="061a4-103">ITipAutocompleteProvider interface</span></span>

<span data-ttu-id="061a4-104">Administra el lado de la aplicación de la integración de autocompletar del panel de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="061a4-104">Manages the application's side of the Text Input Panel auto complete integration.</span></span>

## <a name="members"></a><span data-ttu-id="061a4-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="061a4-105">Members</span></span>

<span data-ttu-id="061a4-106">La interfaz **ITipAutocompleteProvider** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="061a4-106">The **ITipAutocompleteProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="061a4-107">**ITipAutocompleteProvider** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="061a4-107">**ITipAutocompleteProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="061a4-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="061a4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="061a4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="061a4-109">Methods</span></span>

<span data-ttu-id="061a4-110">La interfaz **ITipAutocompleteProvider** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="061a4-110">The **ITipAutocompleteProvider** interface has these methods.</span></span>



| <span data-ttu-id="061a4-111">Método</span><span class="sxs-lookup"><span data-stu-id="061a4-111">Method</span></span>                                                                  | <span data-ttu-id="061a4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="061a4-112">Description</span></span>                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="061a4-113">**Feria**</span><span class="sxs-lookup"><span data-stu-id="061a4-113">**Show**</span></span>](itipautocompleteprovider-show.md)                           | <span data-ttu-id="061a4-114">Muestra u oculta la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="061a4-114">Displays or hides the auto complete list.</span></span><br/>                                                                 |
| [<span data-ttu-id="061a4-115">**UpdatePendingText**</span><span class="sxs-lookup"><span data-stu-id="061a4-115">**UpdatePendingText**</span></span>](itipautocompleteprovider-updatependingtext.md) | <span data-ttu-id="061a4-116">Lo usa el cliente de Autocompletar para notificar a la aplicación el texto que un usuario ha tachado en el panel de entrada.</span><span class="sxs-lookup"><span data-stu-id="061a4-116">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="061a4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="061a4-117">Requirements</span></span>



| <span data-ttu-id="061a4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="061a4-118">Requirement</span></span> | <span data-ttu-id="061a4-119">Value</span><span class="sxs-lookup"><span data-stu-id="061a4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="061a4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="061a4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="061a4-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="061a4-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="061a4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="061a4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="061a4-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="061a4-123">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="061a4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="061a4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="061a4-125"><dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="061a4-125"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="061a4-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="061a4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="061a4-127"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="061a4-127"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="061a4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="061a4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061a4-129">Referencia del panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="061a4-129">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> <dt>

[<span data-ttu-id="061a4-130">**Interfaz ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="061a4-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> </dl>

 

