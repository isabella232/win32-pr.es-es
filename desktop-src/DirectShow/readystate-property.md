---
description: La propiedad ReadyState recupera el ReadyState del objeto MSWebDVD.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Propiedad ReadyState (Ocidl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679438"
---
# <a name="readystate-property"></a><span data-ttu-id="96696-103">Propiedad ReadyState</span><span class="sxs-lookup"><span data-stu-id="96696-103">ReadyState Property</span></span>

> [!Note]  
> <span data-ttu-id="96696-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="96696-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="96696-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="96696-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="96696-106">La `ReadyState` propiedad recupera el ReadyState del objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="96696-106">The `ReadyState` property retrieves the ReadyState of the **MSWebDVD** object.</span></span>

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a><span data-ttu-id="96696-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96696-107">Return Value</span></span>

<span data-ttu-id="96696-108">Devuelve un valor entero que representa el objeto ReadyState del control.</span><span class="sxs-lookup"><span data-stu-id="96696-108">Returns an integer value representing the control's ReadyState.</span></span>



| <span data-ttu-id="96696-109">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="96696-109">Return code</span></span> | <span data-ttu-id="96696-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="96696-110">Description</span></span>                                               |
|-------------|-----------------------------------------------------------|
| <span data-ttu-id="96696-111">0</span><span class="sxs-lookup"><span data-stu-id="96696-111">0</span></span>           | <span data-ttu-id="96696-112">Estado de inicialización predeterminado.</span><span class="sxs-lookup"><span data-stu-id="96696-112">Default initialization state.</span></span>                             |
| <span data-ttu-id="96696-113">1</span><span class="sxs-lookup"><span data-stu-id="96696-113">1</span></span>           | <span data-ttu-id="96696-114">El objeto está cargando sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="96696-114">Object is loading its properties.</span></span>                         |
| <span data-ttu-id="96696-115">2</span><span class="sxs-lookup"><span data-stu-id="96696-115">2</span></span>           | <span data-ttu-id="96696-116">El objeto se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="96696-116">Object has been initialized.</span></span>                              |
| <span data-ttu-id="96696-117">3</span><span class="sxs-lookup"><span data-stu-id="96696-117">3</span></span>           | <span data-ttu-id="96696-118">El objeto es interactivo, pero no todos sus datos están disponibles.</span><span class="sxs-lookup"><span data-stu-id="96696-118">Object is interactive, but not all its data is available.</span></span> |
| <span data-ttu-id="96696-119">4</span><span class="sxs-lookup"><span data-stu-id="96696-119">4</span></span>           | <span data-ttu-id="96696-120">El objeto ha recibido todos sus datos.</span><span class="sxs-lookup"><span data-stu-id="96696-120">Object has received all its data.</span></span>                         |



 

## <a name="remarks"></a><span data-ttu-id="96696-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96696-121">Remarks</span></span>

<span data-ttu-id="96696-122">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="96696-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="96696-123">Cualquier objeto incrustado en una página web expone la `ReadyState` propiedad.</span><span class="sxs-lookup"><span data-stu-id="96696-123">Any object embedded in a Web page exposes the `ReadyState` property.</span></span>

## <a name="requirements"></a><span data-ttu-id="96696-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96696-124">Requirements</span></span>



| <span data-ttu-id="96696-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="96696-125">Requirement</span></span> | <span data-ttu-id="96696-126">Value</span><span class="sxs-lookup"><span data-stu-id="96696-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96696-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96696-127">Header</span></span><br/> | <dl> <span data-ttu-id="96696-128"><dt>Ocidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96696-128"><dt>Ocidl.h</dt></span></span> </dl> |



 

 




