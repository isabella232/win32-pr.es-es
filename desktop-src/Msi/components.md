---
description: El objeto de componente representa una instancia única de un componente que está disponible para la enumeración.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Objeto de componente
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653612"
---
# <a name="component-object"></a><span data-ttu-id="03da9-103">Objeto de componente</span><span class="sxs-lookup"><span data-stu-id="03da9-103">Component object</span></span>

<span data-ttu-id="03da9-104">El objeto de componente representa una instancia única de un componente que está disponible para la enumeración.</span><span class="sxs-lookup"><span data-stu-id="03da9-104">The Component object represents a unique instance of a component that is available for enumeration.</span></span>

<span data-ttu-id="03da9-105">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="03da9-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="03da9-106">Este objeto está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="03da9-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="03da9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="03da9-107">Members</span></span>

<span data-ttu-id="03da9-108">El objeto de **componente** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="03da9-108">The **Component** object has these types of members:</span></span>

-   [<span data-ttu-id="03da9-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03da9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03da9-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03da9-110">Properties</span></span>

<span data-ttu-id="03da9-111">El objeto de **componente** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="03da9-111">The **Component** object has these properties.</span></span>



| <span data-ttu-id="03da9-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="03da9-112">Property</span></span>                                                    | <span data-ttu-id="03da9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="03da9-113">Description</span></span>                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03da9-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="03da9-114">**ComponentCode**</span></span>](component-componentcode.md)<br/> | <span data-ttu-id="03da9-115">Código de componente del componente en cuestión.</span><span class="sxs-lookup"><span data-stu-id="03da9-115">The component code of the component in question.</span></span><br/>                               |
| [<span data-ttu-id="03da9-116">**Context**</span><span class="sxs-lookup"><span data-stu-id="03da9-116">**Context**</span></span>](component-context.md)<br/>             | <span data-ttu-id="03da9-117">Contexto que se ha determinado que es aplicable al componente en cuestión.</span><span class="sxs-lookup"><span data-stu-id="03da9-117">The context that was determined to be applicable to the component in question.</span></span><br/> |
| [<span data-ttu-id="03da9-118">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="03da9-118">**UserSID**</span></span>](component-usersid.md)<br/>             | <span data-ttu-id="03da9-119">SID de usuario para el componente enumerado.</span><span class="sxs-lookup"><span data-stu-id="03da9-119">The user SID for the enumerated component.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="03da9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03da9-120">Requirements</span></span>



| <span data-ttu-id="03da9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="03da9-121">Requirement</span></span> | <span data-ttu-id="03da9-122">Value</span><span class="sxs-lookup"><span data-stu-id="03da9-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03da9-123">Versión</span><span class="sxs-lookup"><span data-stu-id="03da9-123">Version</span></span><br/> | <span data-ttu-id="03da9-124">Windows Installer 5,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="03da9-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="03da9-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03da9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="03da9-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03da9-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="03da9-127">IID</span><span class="sxs-lookup"><span data-stu-id="03da9-127">IID</span></span><br/>     | <span data-ttu-id="03da9-128">IID \_ IComponent se define como 000C1097-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="03da9-128">IID\_IComponent is defined as 000C1097-0000-0000-C000-000000000046</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="03da9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="03da9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03da9-130">Usar la interfaz de automatización</span><span class="sxs-lookup"><span data-stu-id="03da9-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="03da9-131">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="03da9-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




