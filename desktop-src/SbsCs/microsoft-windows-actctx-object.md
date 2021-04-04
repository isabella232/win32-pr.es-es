---
description: El objeto Microsoft. Windows. ActCtx hace referencia a los manifiestos y proporciona una manera de que los motores de scripting tengan acceso a los ensamblados en paralelo. El objeto Microsoft. Windows. ActCtx se puede usar para crear una instancia de un ensamblado en paralelo con componentes COM.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Objeto Microsoft. Windows. ActCtx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908830"
---
# <a name="microsoftwindowsactctx-object"></a><span data-ttu-id="bef5d-104">Objeto Microsoft. Windows. ActCtx</span><span class="sxs-lookup"><span data-stu-id="bef5d-104">Microsoft.Windows.ActCtx object</span></span>

<span data-ttu-id="bef5d-105">El objeto **Microsoft. Windows. ActCtx** hace referencia a los manifiestos y proporciona una manera de que los motores de scripting tengan acceso a los ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="bef5d-105">The **Microsoft.Windows.ActCtx** object references manifests and provides a way for scripting engines to access side-by-side assemblies.</span></span> <span data-ttu-id="bef5d-106">El objeto **Microsoft. Windows. ActCtx** se puede usar para crear una instancia de un ensamblado en paralelo con componentes com.</span><span class="sxs-lookup"><span data-stu-id="bef5d-106">The **Microsoft.Windows.ActCtx** object can be used to create an instance of a side-by-side assembly with COM components.</span></span>

<span data-ttu-id="bef5d-107">El objeto **Microsoft. Windows. ActCtx** se incluye como un ensamblado en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bef5d-107">The **Microsoft.Windows.ActCtx** object comes as an assembly in Windows Server 2003.</span></span> <span data-ttu-id="bef5d-108">También puede instalarse mediante aplicaciones que usan el Windows Installer para la configuración e incluirla como módulo de combinación en su paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="bef5d-108">It can also be installed by applications that use the Windows Installer for setup and include it as a merge module in their installation package.</span></span>

## <a name="members"></a><span data-ttu-id="bef5d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="bef5d-109">Members</span></span>

<span data-ttu-id="bef5d-110">El objeto **Microsoft. Windows. ActCtx** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bef5d-110">The **Microsoft.Windows.ActCtx** object has these types of members:</span></span>

-   [<span data-ttu-id="bef5d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="bef5d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="bef5d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bef5d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bef5d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="bef5d-113">Methods</span></span>

<span data-ttu-id="bef5d-114">El objeto **Microsoft. Windows. ActCtx** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bef5d-114">The **Microsoft.Windows.ActCtx** object has these methods.</span></span>



| <span data-ttu-id="bef5d-115">Método</span><span class="sxs-lookup"><span data-stu-id="bef5d-115">Method</span></span>                               | <span data-ttu-id="bef5d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bef5d-116">Description</span></span>                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="bef5d-117">**DataSpace**</span><span class="sxs-lookup"><span data-stu-id="bef5d-117">**CreateObject**</span></span>](createobject.md) | <span data-ttu-id="bef5d-118">Crea un objeto en el contexto del manifiesto actual.</span><span class="sxs-lookup"><span data-stu-id="bef5d-118">Creates an object in the context of the current manifest.</span></span><br/>            |
| [<span data-ttu-id="bef5d-119">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="bef5d-119">**GetObject**</span></span>](getobject.md)       | <span data-ttu-id="bef5d-120">Obtiene una instancia de un objeto **Microsoft. Windows. ActCtx** existente.</span><span class="sxs-lookup"><span data-stu-id="bef5d-120">Gets an instance of an existing **Microsoft.Windows.ActCtx** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bef5d-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bef5d-121">Properties</span></span>

<span data-ttu-id="bef5d-122">El objeto **Microsoft. Windows. ActCtx** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bef5d-122">The **Microsoft.Windows.ActCtx** object has these properties.</span></span>



| <span data-ttu-id="bef5d-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bef5d-123">Property</span></span>                                | <span data-ttu-id="bef5d-124">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="bef5d-124">Access type</span></span>          | <span data-ttu-id="bef5d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="bef5d-125">Description</span></span>                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [<span data-ttu-id="bef5d-126">**Manifiesto**</span><span class="sxs-lookup"><span data-stu-id="bef5d-126">**Manifest**</span></span>](manifest.md)<br/> | <span data-ttu-id="bef5d-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bef5d-127">Read-only</span></span><br/> | <span data-ttu-id="bef5d-128">Obtiene el contexto de activación activo.</span><span class="sxs-lookup"><span data-stu-id="bef5d-128">Gets the active activation context.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bef5d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bef5d-129">Requirements</span></span>



| <span data-ttu-id="bef5d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bef5d-130">Requirement</span></span> | <span data-ttu-id="bef5d-131">Value</span><span class="sxs-lookup"><span data-stu-id="bef5d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bef5d-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bef5d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bef5d-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bef5d-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="bef5d-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bef5d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bef5d-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bef5d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




