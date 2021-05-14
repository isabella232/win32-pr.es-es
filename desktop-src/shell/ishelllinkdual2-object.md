---
description: Extiende el objeto ShellLinkObject y admite una propiedad adicional.
title: Objeto IShellLinkDual2 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellLinkDual2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 8a63552c-6bce-4583-8df8-a7f7731b35eb
ms.openlocfilehash: 47dc46d20fc6cf5096a38ccfd1790957f1fdd318
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842646"
---
# <a name="ishelllinkdual2-object"></a><span data-ttu-id="8fcf3-103">Objeto IShellLinkDual2</span><span class="sxs-lookup"><span data-stu-id="8fcf3-103">IShellLinkDual2 object</span></span>

<span data-ttu-id="8fcf3-104">Extiende el objeto [**ShellLinkObject**](shelllinkobject-object.md) y admite una propiedad adicional.</span><span class="sxs-lookup"><span data-stu-id="8fcf3-104">Extends the [**ShellLinkObject**](shelllinkobject-object.md) object and supports one additional property.</span></span>

## <a name="members"></a><span data-ttu-id="8fcf3-105">Members</span><span class="sxs-lookup"><span data-stu-id="8fcf3-105">Members</span></span>

<span data-ttu-id="8fcf3-106">El **objeto IShellLinkDual2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8fcf3-106">The **IShellLinkDual2** object has these types of members:</span></span>

-   [<span data-ttu-id="8fcf3-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8fcf3-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fcf3-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8fcf3-108">Properties</span></span>

<span data-ttu-id="8fcf3-109">El **objeto IShellLinkDual2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8fcf3-109">The **IShellLinkDual2** object has these properties.</span></span>



| <span data-ttu-id="8fcf3-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8fcf3-110">Property</span></span>                                            | <span data-ttu-id="8fcf3-111">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="8fcf3-111">Access type</span></span>          | <span data-ttu-id="8fcf3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fcf3-112">Description</span></span>                                   |
|:----------------------------------------------------|:---------------------|:----------------------------------------------|
| [<span data-ttu-id="8fcf3-113">**Destino**</span><span class="sxs-lookup"><span data-stu-id="8fcf3-113">**Target**</span></span>](ishelllinkdual2-target.md)<br/> | <span data-ttu-id="8fcf3-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="8fcf3-114">Read-only</span></span><br/> | <span data-ttu-id="8fcf3-115">Contiene el destino del objeto de vínculo.</span><span class="sxs-lookup"><span data-stu-id="8fcf3-115">Contains the link object's target.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8fcf3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fcf3-116">Requirements</span></span>



| <span data-ttu-id="8fcf3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fcf3-117">Requirement</span></span> | <span data-ttu-id="8fcf3-118">Value</span><span class="sxs-lookup"><span data-stu-id="8fcf3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcf3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fcf3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8fcf3-120">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="8fcf3-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8fcf3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fcf3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8fcf3-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8fcf3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8fcf3-123">Header</span><span class="sxs-lookup"><span data-stu-id="8fcf3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fcf3-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf3-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8fcf3-125">Idl</span><span class="sxs-lookup"><span data-stu-id="8fcf3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8fcf3-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf3-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8fcf3-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8fcf3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fcf3-128"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf3-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




