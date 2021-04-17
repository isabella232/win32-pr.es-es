---
description: El objeto ComponentInfo representa los detalles adicionales sobre un componente que se puede obtener a través de una llamada de MsiGetComponentPathEx.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: Objeto ComponentInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653613"
---
# <a name="componentinfo-object"></a><span data-ttu-id="23dbe-103">Objeto ComponentInfo</span><span class="sxs-lookup"><span data-stu-id="23dbe-103">ComponentInfo object</span></span>

<span data-ttu-id="23dbe-104">El objeto ComponentInfo representa los detalles adicionales sobre un componente que se puede obtener a través de una llamada de MsiGetComponentPathEx.</span><span class="sxs-lookup"><span data-stu-id="23dbe-104">The ComponentInfo object represents additional details about a component that may be obtained via a call from MsiGetComponentPathEx.</span></span>

<span data-ttu-id="23dbe-105">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="23dbe-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="23dbe-106">Este objeto está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="23dbe-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="23dbe-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="23dbe-107">Members</span></span>

<span data-ttu-id="23dbe-108">El objeto **ComponentInfo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="23dbe-108">The **ComponentInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="23dbe-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23dbe-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23dbe-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23dbe-110">Properties</span></span>

<span data-ttu-id="23dbe-111">El objeto **ComponentInfo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="23dbe-111">The **ComponentInfo** object has these properties.</span></span>



| <span data-ttu-id="23dbe-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="23dbe-112">Property</span></span>                                                        | <span data-ttu-id="23dbe-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="23dbe-113">Description</span></span>                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="23dbe-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="23dbe-114">**ComponentCode**</span></span>](componentinfo-componentcode.md)<br/> | <span data-ttu-id="23dbe-115">Código de componente del componente en cuestión.</span><span class="sxs-lookup"><span data-stu-id="23dbe-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="23dbe-116">**Ruta**</span><span class="sxs-lookup"><span data-stu-id="23dbe-116">**Path**</span></span>](componentinfo-componentcode.md)<br/>          | <span data-ttu-id="23dbe-117">Ruta de acceso del componente.</span><span class="sxs-lookup"><span data-stu-id="23dbe-117">The path of the component.</span></span><br/>                       |
| [<span data-ttu-id="23dbe-118">**State**</span><span class="sxs-lookup"><span data-stu-id="23dbe-118">**State**</span></span>](componentinfo-state.md)<br/>                 | <span data-ttu-id="23dbe-119">Estado del componente.</span><span class="sxs-lookup"><span data-stu-id="23dbe-119">The state of the component.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="23dbe-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23dbe-120">Requirements</span></span>



| <span data-ttu-id="23dbe-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="23dbe-121">Requirement</span></span> | <span data-ttu-id="23dbe-122">Value</span><span class="sxs-lookup"><span data-stu-id="23dbe-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23dbe-123">Versión</span><span class="sxs-lookup"><span data-stu-id="23dbe-123">Version</span></span><br/> | <span data-ttu-id="23dbe-124">Windows Installer 5,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="23dbe-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="23dbe-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23dbe-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="23dbe-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23dbe-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="23dbe-127">IID</span><span class="sxs-lookup"><span data-stu-id="23dbe-127">IID</span></span><br/>     | <span data-ttu-id="23dbe-128">IID \_ IComponentInfo se define como 000C1099-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="23dbe-128">IID\_IComponentInfo is defined as 000C1099-0000-0000-C000-000000000046</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="23dbe-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="23dbe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23dbe-130">Usar la interfaz de automatización</span><span class="sxs-lookup"><span data-stu-id="23dbe-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="23dbe-131">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="23dbe-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




