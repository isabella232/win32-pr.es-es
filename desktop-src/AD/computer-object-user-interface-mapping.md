---
title: Asignación de interfaz de usuario de objetos de equipo
description: En las tablas siguientes se enumeran los elementos de las hojas de propiedades de objetos de equipo en el complemento usuarios y equipos de Active Directory.
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789610"
---
# <a name="computer-object-user-interface-mapping"></a><span data-ttu-id="097d3-103">Asignación de interfaz de usuario de objetos de equipo</span><span class="sxs-lookup"><span data-stu-id="097d3-103">Computer Object User Interface Mapping</span></span>

<span data-ttu-id="097d3-104">En las tablas siguientes se enumeran los elementos de las hojas de propiedades de objetos de equipo en el complemento usuarios y equipos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="097d3-104">The following tables list elements of the Computer object property sheets in the Active Directory Users and Computers snap-in.</span></span>

## <a name="general-property-sheet"></a><span data-ttu-id="097d3-105">Hoja de propiedades general</span><span class="sxs-lookup"><span data-stu-id="097d3-105">General Property Sheet</span></span>

<span data-ttu-id="097d3-106">En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **General** .</span><span class="sxs-lookup"><span data-stu-id="097d3-106">The following table lists the UI labels of the **General** property sheet.</span></span>



| <span data-ttu-id="097d3-107">Etiqueta de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="097d3-107">UI label</span></span>                         | <span data-ttu-id="097d3-108">Active Directory Domain Services atributo)</span><span class="sxs-lookup"><span data-stu-id="097d3-108">Active Directory Domain Services attribute</span></span> | <span data-ttu-id="097d3-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="097d3-109">Comments</span></span>                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="097d3-110">Nombre del equipo (anterior a Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="097d3-110">Computer Name (pre-Windows 2000)</span></span> | <span data-ttu-id="097d3-111">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="097d3-111">sAMAccountName</span></span>                             |                                                  |
| <span data-ttu-id="097d3-112">Nombre DNS</span><span class="sxs-lookup"><span data-stu-id="097d3-112">DNS Name</span></span>                         | <span data-ttu-id="097d3-113">dNSHostName</span><span class="sxs-lookup"><span data-stu-id="097d3-113">dNSHostName</span></span>                                |                                                  |
| <span data-ttu-id="097d3-114">Role</span><span class="sxs-lookup"><span data-stu-id="097d3-114">Role</span></span>                             | <span data-ttu-id="097d3-115">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="097d3-115">userAccountControl</span></span>                         | <span data-ttu-id="097d3-116">Alterna un bit en la máscara de bits de userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="097d3-116">Toggles a bit in the userAccountControl bitmask.</span></span> |
| <span data-ttu-id="097d3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="097d3-117">Description</span></span>                      | <span data-ttu-id="097d3-118">description</span><span class="sxs-lookup"><span data-stu-id="097d3-118">description</span></span>                                |                                                  |
| <span data-ttu-id="097d3-119">Confiar en equipo para delegación</span><span class="sxs-lookup"><span data-stu-id="097d3-119">Trust Computer for delegation</span></span>    | <span data-ttu-id="097d3-120">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="097d3-120">userAccountControl</span></span>                         | <span data-ttu-id="097d3-121">Alterna un bit en la máscara de bits de userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="097d3-121">Toggles a bit in the userAccountControl bitmask.</span></span> |



 

## <a name="location-property-sheet"></a><span data-ttu-id="097d3-122">Ubicación (hoja de propiedades)</span><span class="sxs-lookup"><span data-stu-id="097d3-122">Location Property Sheet</span></span>

<span data-ttu-id="097d3-123">En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **Location** .</span><span class="sxs-lookup"><span data-stu-id="097d3-123">The following table lists the UI labels of the **Location** property sheet.</span></span>



| <span data-ttu-id="097d3-124">Etiqueta de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="097d3-124">UI label</span></span> | <span data-ttu-id="097d3-125">Active Directory Domain Services atributo)</span><span class="sxs-lookup"><span data-stu-id="097d3-125">Active Directory Domain Services attribute</span></span> |
|----------|--------------------------------------------|
| <span data-ttu-id="097d3-126">Location</span><span class="sxs-lookup"><span data-stu-id="097d3-126">Location</span></span> | <span data-ttu-id="097d3-127">ubicación</span><span class="sxs-lookup"><span data-stu-id="097d3-127">location</span></span>                                   |



 

## <a name="member-of-property-sheet"></a><span data-ttu-id="097d3-128">Miembro de la hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="097d3-128">Member Of Property Sheet</span></span>

<span data-ttu-id="097d3-129">En la tabla siguiente se muestran las etiquetas de la interfaz de usuario del **miembro de** la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="097d3-129">The following table lists the UI labels of the **Member Of** property sheet.</span></span>



| <span data-ttu-id="097d3-130">Etiqueta de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="097d3-130">UI label</span></span>          | <span data-ttu-id="097d3-131">Active Directory Domain Services atributo)</span><span class="sxs-lookup"><span data-stu-id="097d3-131">Active Directory Domain Services attribute</span></span> | <span data-ttu-id="097d3-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="097d3-132">Comments</span></span>                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="097d3-133">Miembro de</span><span class="sxs-lookup"><span data-stu-id="097d3-133">Member of</span></span>         | <span data-ttu-id="097d3-134">memberOf</span><span class="sxs-lookup"><span data-stu-id="097d3-134">memberOf</span></span>                                   | <span data-ttu-id="097d3-135">Incluye todos los grupos de la lista de interfaz de usuario, excepto el grupo principal, que se representa en el AD mediante el atributo [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) .</span><span class="sxs-lookup"><span data-stu-id="097d3-135">Includes all of the groups in the UI list, except the primary group, which is represented in the AD through the [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) attribute.</span></span> |
| <span data-ttu-id="097d3-136">Establecer grupo principal</span><span class="sxs-lookup"><span data-stu-id="097d3-136">Set Primary Group</span></span> | <span data-ttu-id="097d3-137">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="097d3-137">primaryGroupID</span></span>                             | <span data-ttu-id="097d3-138">LDAP: vinculado a [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del grupo principal.</span><span class="sxs-lookup"><span data-stu-id="097d3-138">LDAP: Tied to [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) of the primary group.</span></span>                                                                                  |



 

## <a name="operating-system-property-sheet"></a><span data-ttu-id="097d3-139">Hoja de propiedades del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="097d3-139">Operating System Property Sheet</span></span>

<span data-ttu-id="097d3-140">En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **del sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="097d3-140">The following table lists the UI labels of the **Operating System** property sheet.</span></span>



| <span data-ttu-id="097d3-141">Etiqueta de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="097d3-141">UI label</span></span>     | <span data-ttu-id="097d3-142">Active Directory Domain Services atributo)</span><span class="sxs-lookup"><span data-stu-id="097d3-142">Active Directory Domain Services attribute</span></span> |
|--------------|--------------------------------------------|
| <span data-ttu-id="097d3-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="097d3-143">Name</span></span>         | <span data-ttu-id="097d3-144">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="097d3-144">operatingSystem</span></span>                            |
| <span data-ttu-id="097d3-145">Versión</span><span class="sxs-lookup"><span data-stu-id="097d3-145">Version</span></span>      | <span data-ttu-id="097d3-146">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="097d3-146">operatingSystemVersion</span></span>                     |
| <span data-ttu-id="097d3-147">Service Pack</span><span class="sxs-lookup"><span data-stu-id="097d3-147">Service Pack</span></span> | <span data-ttu-id="097d3-148">operatingSystemServicePack</span><span class="sxs-lookup"><span data-stu-id="097d3-148">operatingSystemServicePack</span></span>                 |



 

 

 