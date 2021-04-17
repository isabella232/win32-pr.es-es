---
description: La interfaz ITablet3 habilita la consulta de multitoque para la entrada.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: Interfaz ITablet3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716908"
---
# <a name="itablet3-interface"></a><span data-ttu-id="80ecd-103">Interfaz ITablet3</span><span class="sxs-lookup"><span data-stu-id="80ecd-103">ITablet3 interface</span></span>

<span data-ttu-id="80ecd-104">La interfaz ITablet3 habilita la consulta de multitoque para la entrada.</span><span class="sxs-lookup"><span data-stu-id="80ecd-104">The ITablet3 interface enables multitouch querying for input.</span></span>

## <a name="members"></a><span data-ttu-id="80ecd-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="80ecd-105">Members</span></span>

<span data-ttu-id="80ecd-106">La interfaz **ITablet3** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="80ecd-106">The **ITablet3** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="80ecd-107">**ITablet3** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="80ecd-107">**ITablet3** also has these types of members:</span></span>

-   [<span data-ttu-id="80ecd-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="80ecd-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="80ecd-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="80ecd-109">Methods</span></span>

<span data-ttu-id="80ecd-110">La interfaz **ITablet3** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="80ecd-110">The **ITablet3** interface has these methods.</span></span>



| <span data-ttu-id="80ecd-111">Método</span><span class="sxs-lookup"><span data-stu-id="80ecd-111">Method</span></span>                                                  | <span data-ttu-id="80ecd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="80ecd-112">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="80ecd-113">**GetMaximumCursors**</span><span class="sxs-lookup"><span data-stu-id="80ecd-113">**GetMaximumCursors**</span></span>](itablet3-getmaximumcursors.md) | <span data-ttu-id="80ecd-114">Recupera el número máximo de entradas admitidas.</span><span class="sxs-lookup"><span data-stu-id="80ecd-114">Retrieves the maximum number of inputs supported.</span></span><br/>        |
| [<span data-ttu-id="80ecd-115">**isMultiTouch**</span><span class="sxs-lookup"><span data-stu-id="80ecd-115">**isMultiTouch**</span></span>](itablet3-ismultitouch.md)           | <span data-ttu-id="80ecd-116">Indica si multitoque está habilitado para este objeto.</span><span class="sxs-lookup"><span data-stu-id="80ecd-116">Indicates whether multitouch is enabled for this object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="80ecd-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80ecd-117">Remarks</span></span>

<span data-ttu-id="80ecd-118">Los desarrolladores no deben usar esta interfaz</span><span class="sxs-lookup"><span data-stu-id="80ecd-118">Developers should not use this interface</span></span>

<span data-ttu-id="80ecd-119">En el código siguiente se describe cómo se define la interfaz **ITablet3** .</span><span class="sxs-lookup"><span data-stu-id="80ecd-119">The following code describes how the **ITablet3** interface is defined.</span></span>

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a><span data-ttu-id="80ecd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80ecd-120">Requirements</span></span>



| <span data-ttu-id="80ecd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="80ecd-121">Requirement</span></span> | <span data-ttu-id="80ecd-122">Value</span><span class="sxs-lookup"><span data-stu-id="80ecd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80ecd-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80ecd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="80ecd-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="80ecd-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="80ecd-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80ecd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="80ecd-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="80ecd-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="80ecd-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80ecd-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="80ecd-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80ecd-128"><dt>Wisptis.exe</dt></span></span> </dl> |



 

