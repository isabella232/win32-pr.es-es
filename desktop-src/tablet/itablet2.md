---
description: Extiende la interfaz ITablet.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: Interfaz ITablet2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720678"
---
# <a name="itablet2-interface"></a><span data-ttu-id="6a73a-103">Interfaz ITablet2</span><span class="sxs-lookup"><span data-stu-id="6a73a-103">ITablet2 interface</span></span>

<span data-ttu-id="6a73a-104">Extiende la [**interfaz ITablet**](itablet.md).</span><span class="sxs-lookup"><span data-stu-id="6a73a-104">Extends the [**ITablet Interface**](itablet.md).</span></span>

## <a name="members"></a><span data-ttu-id="6a73a-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a73a-105">Members</span></span>

<span data-ttu-id="6a73a-106">La interfaz **ITablet2** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6a73a-106">The **ITablet2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6a73a-107">**ITablet2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6a73a-107">**ITablet2** also has these types of members:</span></span>

-   [<span data-ttu-id="6a73a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6a73a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a73a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6a73a-109">Methods</span></span>

<span data-ttu-id="6a73a-110">La interfaz **ITablet2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6a73a-110">The **ITablet2** interface has these methods.</span></span>



| <span data-ttu-id="6a73a-111">Método</span><span class="sxs-lookup"><span data-stu-id="6a73a-111">Method</span></span>                                          | <span data-ttu-id="6a73a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a73a-112">Description</span></span>                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a73a-113">**GetDeviceKind**</span><span class="sxs-lookup"><span data-stu-id="6a73a-113">**GetDeviceKind**</span></span>](itablet2-getdevicekind.md) | <span data-ttu-id="6a73a-114">Devuelve el tipo de dispositivo de hardware que representa el objeto de tableta, como el mouse, el lápiz o la entrada táctil.</span><span class="sxs-lookup"><span data-stu-id="6a73a-114">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a73a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a73a-115">Remarks</span></span>

<span data-ttu-id="6a73a-116">Esta interfaz se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a73a-116">This interface was introduced in Windows Vista.</span></span>

<span data-ttu-id="6a73a-117">Los desarrolladores no deben utilizar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="6a73a-117">Developers should not use this interface.</span></span>

<span data-ttu-id="6a73a-118">En el código siguiente se describe cómo se define la interfaz **ITablet2** .</span><span class="sxs-lookup"><span data-stu-id="6a73a-118">The following code describes how the **ITablet2** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a><span data-ttu-id="6a73a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a73a-119">Requirements</span></span>



| <span data-ttu-id="6a73a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a73a-120">Requirement</span></span> | <span data-ttu-id="6a73a-121">Value</span><span class="sxs-lookup"><span data-stu-id="6a73a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a73a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a73a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6a73a-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a73a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6a73a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a73a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6a73a-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6a73a-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6a73a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a73a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a73a-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a73a-127"><dt>Wisptis.exe</dt></span></span> </dl> |



 

