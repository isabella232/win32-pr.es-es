---
title: Asignación de la interfaz de usuario de unidades organizativas
description: En este tema se describen las hojas de propiedades de los objetos de la unidad organizativa (OU) en el complemento usuarios y equipos de Active Directory.
ms.assetid: 105c0f01-55d5-4dc2-887e-5e204ba82c4c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8b08014d141c2182f47a5e3a40ebb9a18004ba
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904483"
---
# <a name="organizational-unit-user-interface-mapping"></a><span data-ttu-id="ed712-103">Asignación de la interfaz de usuario de unidades organizativas</span><span class="sxs-lookup"><span data-stu-id="ed712-103">Organizational Unit User Interface Mapping</span></span>

<span data-ttu-id="ed712-104">En este tema se describen las hojas de propiedades de los objetos de la unidad organizativa (OU) en el complemento usuarios y equipos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ed712-104">This topic describes the Organizational Unit (OU) object property sheets in the Active Directory Users and Computers snap-in.</span></span>

## <a name="general-property-sheet"></a><span data-ttu-id="ed712-105">Hoja de propiedades general</span><span class="sxs-lookup"><span data-stu-id="ed712-105">General Property Sheet</span></span>

<span data-ttu-id="ed712-106">En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **General** .</span><span class="sxs-lookup"><span data-stu-id="ed712-106">The following table shows the UI labels of the **General** property sheet.</span></span>



| <span data-ttu-id="ed712-107">Etiqueta de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="ed712-107">UI label</span></span>        | <span data-ttu-id="ed712-108">Atributo en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ed712-108">Attribute in Active Directory Domain Services</span></span> |
|-----------------|-----------------------------------------------|
| <span data-ttu-id="ed712-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed712-109">Description</span></span>     | [<span data-ttu-id="ed712-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ed712-110">**Description**</span></span>](/windows/desktop/ADSchema/a-description)     |
| <span data-ttu-id="ed712-111">Calle</span><span class="sxs-lookup"><span data-stu-id="ed712-111">Street</span></span>          | [<span data-ttu-id="ed712-112">**Dirección postal**</span><span class="sxs-lookup"><span data-stu-id="ed712-112">**Street-Address**</span></span>](/windows/desktop/ADSchema/a-street)       |
| <span data-ttu-id="ed712-113">City (Ciudad)</span><span class="sxs-lookup"><span data-stu-id="ed712-113">City</span></span>            | [<span data-ttu-id="ed712-114">**Localidad: nombre**</span><span class="sxs-lookup"><span data-stu-id="ed712-114">**Locality-Name**</span></span>](/windows/desktop/ADSchema/a-l)             |
| <span data-ttu-id="ed712-115">Estado o provincia</span><span class="sxs-lookup"><span data-stu-id="ed712-115">State/Province</span></span>  | [<span data-ttu-id="ed712-116">**Nombre de estado o provincia**</span><span class="sxs-lookup"><span data-stu-id="ed712-116">**State-Or-Province-Name**</span></span>](/windows/desktop/ADSchema/a-st)   |
| <span data-ttu-id="ed712-117">Código postal</span><span class="sxs-lookup"><span data-stu-id="ed712-117">Zip/Postal Code</span></span> | [<span data-ttu-id="ed712-118">**Código postal**</span><span class="sxs-lookup"><span data-stu-id="ed712-118">**Postal-Code**</span></span>](/windows/desktop/ADSchema/a-postalcode)      |
| <span data-ttu-id="ed712-119">País/región</span><span class="sxs-lookup"><span data-stu-id="ed712-119">Country/Region</span></span>  | [<span data-ttu-id="ed712-120">**Nombre del país**</span><span class="sxs-lookup"><span data-stu-id="ed712-120">**Country-Name**</span></span>](/windows/desktop/ADSchema/a-c)              |



 

## <a name="managed-by-property-sheet"></a><span data-ttu-id="ed712-121">Administrado por hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="ed712-121">Managed By Property Sheet</span></span>

<span data-ttu-id="ed712-122">En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **administrado por** .</span><span class="sxs-lookup"><span data-stu-id="ed712-122">The following table shows the UI labels of the **Managed By** property sheet.</span></span>



| <span data-ttu-id="ed712-123">Etiqueta de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="ed712-123">UI label</span></span>         | <span data-ttu-id="ed712-124">Atributo en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ed712-124">Attribute in Active Directory Domain Services</span></span>                                                                                   |
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed712-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="ed712-125">Name</span></span>             | [<span data-ttu-id="ed712-126">**Administrado: por**</span><span class="sxs-lookup"><span data-stu-id="ed712-126">**Managed-By**</span></span>](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| <span data-ttu-id="ed712-127">Office</span><span class="sxs-lookup"><span data-stu-id="ed712-127">Office</span></span>           | <span data-ttu-id="ed712-128">El atributo [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) de la cuenta identificada por **Name**.</span><span class="sxs-lookup"><span data-stu-id="ed712-128">The [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) attribute of the account identified by **Name**.</span></span> |
| <span data-ttu-id="ed712-129">Calle</span><span class="sxs-lookup"><span data-stu-id="ed712-129">Street</span></span>           | <span data-ttu-id="ed712-130">El atributo [**calle-dirección**](/windows/desktop/ADSchema/a-street) de la cuenta identificada por **nombre**.</span><span class="sxs-lookup"><span data-stu-id="ed712-130">The [**Street-Address**](/windows/desktop/ADSchema/a-street) attribute of the account identified by **Name**.</span></span>                                    |
| <span data-ttu-id="ed712-131">City (Ciudad)</span><span class="sxs-lookup"><span data-stu-id="ed712-131">City</span></span>             | <span data-ttu-id="ed712-132">El atributo [**localidad-nombre**](/windows/desktop/ADSchema/a-l) de la cuenta identificada por **nombre**.</span><span class="sxs-lookup"><span data-stu-id="ed712-132">The [**Locality-Name**](/windows/desktop/ADSchema/a-l) attribute of the account identified by **Name**.</span></span>                                          |
| <span data-ttu-id="ed712-133">Estado o provincia</span><span class="sxs-lookup"><span data-stu-id="ed712-133">State/province</span></span>   | <span data-ttu-id="ed712-134">El atributo [**State-or-provincia-Name**](/windows/desktop/ADSchema/a-st) de la cuenta identificada por **Name**.</span><span class="sxs-lookup"><span data-stu-id="ed712-134">The [**State-Or-Province-Name**](/windows/desktop/ADSchema/a-st) attribute of the account identified by **Name**.</span></span>                                |
| <span data-ttu-id="ed712-135">País/región</span><span class="sxs-lookup"><span data-stu-id="ed712-135">Country/region</span></span>   | <span data-ttu-id="ed712-136">El atributo [**Country-name**](/windows/desktop/ADSchema/a-c) de la cuenta identificada por **Name**.</span><span class="sxs-lookup"><span data-stu-id="ed712-136">The [**Country-Name**](/windows/desktop/ADSchema/a-c) attribute of the account identified by **Name**.</span></span>                                           |
| <span data-ttu-id="ed712-137">Número de teléfono</span><span class="sxs-lookup"><span data-stu-id="ed712-137">Telephone number</span></span> | <span data-ttu-id="ed712-138">El atributo de [**número de teléfono**](/windows/desktop/ADSchema/a-telephonenumber) de la cuenta identificada por **nombre**.</span><span class="sxs-lookup"><span data-stu-id="ed712-138">The [**Telephone-Number**](/windows/desktop/ADSchema/a-telephonenumber) attribute of the account identified by **Name**.</span></span>                         |
| <span data-ttu-id="ed712-139">Número de fax</span><span class="sxs-lookup"><span data-stu-id="ed712-139">Fax number</span></span>       | <span data-ttu-id="ed712-140">El atributo [**facsímil-Phone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) de la cuenta identificada por **Name**.</span><span class="sxs-lookup"><span data-stu-id="ed712-140">The [**Facsimile-Telephone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) attribute of the account identified by **Name**.</span></span>      |



 

 

 