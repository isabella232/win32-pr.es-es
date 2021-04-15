---
description: Expone métodos que se usan para inicializar una lista de elementos usados recientemente (MRU) para un objeto de finalización automática.
title: Interfaz IACLCustomMRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: 54cda8d6cc3c7f1c46d6bce7736160b0da67a4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997680"
---
# <a name="iaclcustommru-interface"></a><span data-ttu-id="5eb5b-103">Interfaz IACLCustomMRU</span><span class="sxs-lookup"><span data-stu-id="5eb5b-103">IACLCustomMRU interface</span></span>

<span data-ttu-id="5eb5b-104">Expone métodos que se usan para inicializar una lista de elementos usados recientemente (MRU) para un objeto de finalización automática.</span><span class="sxs-lookup"><span data-stu-id="5eb5b-104">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span>

## <a name="members"></a><span data-ttu-id="5eb5b-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="5eb5b-105">Members</span></span>

<span data-ttu-id="5eb5b-106">La interfaz **IACLCustomMRU** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5eb5b-106">The **IACLCustomMRU** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5eb5b-107">**IACLCustomMRU** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5eb5b-107">**IACLCustomMRU** also has these types of members:</span></span>

-   [<span data-ttu-id="5eb5b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="5eb5b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5eb5b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5eb5b-109">Methods</span></span>

<span data-ttu-id="5eb5b-110">La interfaz **IACLCustomMRU** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5eb5b-110">The **IACLCustomMRU** interface has these methods.</span></span>



| <span data-ttu-id="5eb5b-111">Método</span><span class="sxs-lookup"><span data-stu-id="5eb5b-111">Method</span></span>                                             | <span data-ttu-id="5eb5b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5eb5b-112">Description</span></span>                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="5eb5b-113">**AddMRUString**</span><span class="sxs-lookup"><span data-stu-id="5eb5b-113">**AddMRUString**</span></span>](iaclcustommru-addmrustring.md) | <span data-ttu-id="5eb5b-114">Agrega una entrada a la lista MRU.</span><span class="sxs-lookup"><span data-stu-id="5eb5b-114">Adds an entry to the MRU list.</span></span><br/>                               |
| [<span data-ttu-id="5eb5b-115">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="5eb5b-115">**Initialize**</span></span>](iaclcustommru-initialize.md)     | <span data-ttu-id="5eb5b-116">Carga una lista de cadenas en la lista MRU del registro.</span><span class="sxs-lookup"><span data-stu-id="5eb5b-116">Loads a list of strings into the MRU list from the registry.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5eb5b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5eb5b-117">Requirements</span></span>



| <span data-ttu-id="5eb5b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eb5b-118">Requirement</span></span> | <span data-ttu-id="5eb5b-119">Value</span><span class="sxs-lookup"><span data-stu-id="5eb5b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5eb5b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5eb5b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5eb5b-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5eb5b-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5eb5b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5eb5b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5eb5b-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5eb5b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
