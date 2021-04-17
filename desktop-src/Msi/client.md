---
description: El objeto de cliente representa una relación entre un componente de y un producto de cliente.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Objeto de cliente
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670894"
---
# <a name="client-object"></a><span data-ttu-id="fb99b-103">Objeto de cliente</span><span class="sxs-lookup"><span data-stu-id="fb99b-103">Client object</span></span>

<span data-ttu-id="fb99b-104">El objeto de cliente representa una relación entre un componente de y un producto de cliente.</span><span class="sxs-lookup"><span data-stu-id="fb99b-104">The Client object represents a relationship between a component and client product.</span></span>

<span data-ttu-id="fb99b-105">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="fb99b-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="fb99b-106">Este objeto está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="fb99b-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="fb99b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb99b-107">Members</span></span>

<span data-ttu-id="fb99b-108">El objeto de **cliente** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fb99b-108">The **Client** object has these types of members:</span></span>

-   [<span data-ttu-id="fb99b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb99b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb99b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb99b-110">Properties</span></span>

<span data-ttu-id="fb99b-111">El objeto de **cliente** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fb99b-111">The **Client** object has these properties.</span></span>



| <span data-ttu-id="fb99b-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb99b-112">Property</span></span>                                                 | <span data-ttu-id="fb99b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb99b-113">Description</span></span>                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="fb99b-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="fb99b-114">**ComponentCode**</span></span>](client-componentcode.md)<br/> | <span data-ttu-id="fb99b-115">Código de componente del componente en cuestión.</span><span class="sxs-lookup"><span data-stu-id="fb99b-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="fb99b-116">**Context**</span><span class="sxs-lookup"><span data-stu-id="fb99b-116">**Context**</span></span>](client-context.md)<br/>             | <span data-ttu-id="fb99b-117">Contexto del producto.</span><span class="sxs-lookup"><span data-stu-id="fb99b-117">The context of the product.</span></span><br/>                      |
| [<span data-ttu-id="fb99b-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="fb99b-118">**ProductCode**</span></span>](client-productcode.md)<br/>     | <span data-ttu-id="fb99b-119">Producto de cliente del componente en cuestión.</span><span class="sxs-lookup"><span data-stu-id="fb99b-119">The client product of the component in question.</span></span><br/> |
| [<span data-ttu-id="fb99b-120">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="fb99b-120">**UserSID**</span></span>](client-usersid.md)<br/>             | <span data-ttu-id="fb99b-121">SID de usuario del componente.</span><span class="sxs-lookup"><span data-stu-id="fb99b-121">The user SID for the component.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="fb99b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb99b-122">Requirements</span></span>



| <span data-ttu-id="fb99b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb99b-123">Requirement</span></span> | <span data-ttu-id="fb99b-124">Value</span><span class="sxs-lookup"><span data-stu-id="fb99b-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb99b-125">Versión</span><span class="sxs-lookup"><span data-stu-id="fb99b-125">Version</span></span><br/> | <span data-ttu-id="fb99b-126">Windows Installer 5,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fb99b-126">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="fb99b-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb99b-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb99b-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb99b-128"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb99b-129">IID</span><span class="sxs-lookup"><span data-stu-id="fb99b-129">IID</span></span><br/>     | <span data-ttu-id="fb99b-130">IID \_ IClient se define como 000C1098-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fb99b-130">IID\_IClient is defined as 000C1098-0000-0000-C000-000000000046</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="fb99b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb99b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb99b-132">Usar la interfaz de automatización</span><span class="sxs-lookup"><span data-stu-id="fb99b-132">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="fb99b-133">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fb99b-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




