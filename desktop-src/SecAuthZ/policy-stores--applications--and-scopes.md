---
description: Los almacenes de directivas de autorización, las aplicaciones y los ámbitos representan diferentes niveles de organización de la Directiva de administrador de autorización.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Almacenes de directivas, aplicaciones y ámbitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908179"
---
# <a name="policy-stores-applications-and-scopes"></a><span data-ttu-id="2a791-103">Almacenes de directivas, aplicaciones y ámbitos</span><span class="sxs-lookup"><span data-stu-id="2a791-103">Policy Stores, Applications, and Scopes</span></span>

<span data-ttu-id="2a791-104">Los almacenes de directivas de autorización, las aplicaciones y los ámbitos representan diferentes niveles de organización de la Directiva de administrador de autorización.</span><span class="sxs-lookup"><span data-stu-id="2a791-104">Authorization policy stores, applications, and scopes represent different levels of organization of Authorization Manager policy.</span></span> <span data-ttu-id="2a791-105">Un almacén de directivas puede contener una o más aplicaciones, y una aplicación puede contener uno o más ámbitos.</span><span class="sxs-lookup"><span data-stu-id="2a791-105">A policy store can contain one or more applications, and an application can contain one or more scopes.</span></span>

-   [<span data-ttu-id="2a791-106">Almacenes de directivas de autorización</span><span class="sxs-lookup"><span data-stu-id="2a791-106">Authorization Policy Stores</span></span>](#authorization-policy-stores)
-   [<span data-ttu-id="2a791-107">Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="2a791-107">Applications</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="2a791-108">Ámbitos</span><span class="sxs-lookup"><span data-stu-id="2a791-108">Scopes</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="2a791-109">Delegación</span><span class="sxs-lookup"><span data-stu-id="2a791-109">Delegation</span></span>](#delegation)
-   [<span data-ttu-id="2a791-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a791-110">Related topics</span></span>](#related-topics)

## <a name="authorization-policy-stores"></a><span data-ttu-id="2a791-111">Almacenes de directivas de autorización</span><span class="sxs-lookup"><span data-stu-id="2a791-111">Authorization Policy Stores</span></span>

<span data-ttu-id="2a791-112">En la API de administrador de autorización, un almacén de directivas de autorización se representa mediante un objeto [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="2a791-112">In the Authorization Manager API, an authorization policy store is represented by an [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="2a791-113">El almacén de directivas de autorización contiene definiciones y asignaciones de aplicaciones, ámbitos, operaciones, tareas, roles y grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="2a791-113">The authorization policy store contains definitions and assignments of applications, scopes, operations, tasks, roles, and user groups.</span></span>

<span data-ttu-id="2a791-114">Un almacén de directivas de autorización puede almacenarse como un archivo XML o en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2a791-114">An authorization policy store can be stored either as an XML file or in Active Directory.</span></span>

<span data-ttu-id="2a791-115">Una aplicación debe inicializar un almacén de directivas de autorización antes de cambiar la información del almacén o de usar la Directiva de la tienda para comprobar el acceso del cliente a los recursos.</span><span class="sxs-lookup"><span data-stu-id="2a791-115">An application must initialize an authorization policy store before changing information in the store or using the store policy to check client access to resources.</span></span>

<span data-ttu-id="2a791-116">Un almacén de directivas de autorización puede contener uno o más objetos [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) , cada uno de los cuales representa una directiva de autorización para una aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="2a791-116">An authorization policy store can contain one or more [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) objects that each represent authorization policy for a specific application.</span></span>

## <a name="applications"></a><span data-ttu-id="2a791-117">APLICACIONES</span><span class="sxs-lookup"><span data-stu-id="2a791-117">Applications</span></span>

<span data-ttu-id="2a791-118">En la API de administrador de autorización, una aplicación se representa mediante un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) .</span><span class="sxs-lookup"><span data-stu-id="2a791-118">In the Authorization Manager API, an application is represented by an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object.</span></span> <span data-ttu-id="2a791-119">Un almacén de directivas de autorización puede contener información de directiva de autorización para muchas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2a791-119">An authorization policy store can contain authorization policy information for many applications.</span></span> <span data-ttu-id="2a791-120">El uso de objetos **IAzApplication** permite almacenar diferentes directivas de autorización para diferentes aplicaciones en un único almacén de directivas.</span><span class="sxs-lookup"><span data-stu-id="2a791-120">Using **IAzApplication** objects allows you to store different authorization policy for different applications in a single policy store.</span></span>

<span data-ttu-id="2a791-121">Un almacén de directivas de autorización debe contener al menos una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a791-121">An authorization policy store must contain at least one application.</span></span>

## <a name="scopes"></a><span data-ttu-id="2a791-122">Ámbitos</span><span class="sxs-lookup"><span data-stu-id="2a791-122">Scopes</span></span>

<span data-ttu-id="2a791-123">En la API de administrador de autorización, un ámbito se representa mediante un objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="2a791-123">In the Authorization Manager API, a scope is represented by an [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span> <span data-ttu-id="2a791-124">Los ámbitos proporcionan un nivel de organización adicional y opcional para una directiva de autorización.</span><span class="sxs-lookup"><span data-stu-id="2a791-124">Scopes provide an additional, optional level of organization for an authorization policy.</span></span> <span data-ttu-id="2a791-125">Una aplicación puede contener uno o más ámbitos, pero no es necesario que tenga (el administrador de autorización proporciona un ámbito predeterminado de toda la aplicación).</span><span class="sxs-lookup"><span data-stu-id="2a791-125">An application can contain one or more scopes, but need not contain any (Authorization Manager provides a default, application-wide scope).</span></span>

<span data-ttu-id="2a791-126">Un ámbito es una subdivisión dentro de una aplicación que separa los recursos de otros recursos utilizados por esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a791-126">A scope is a subdivision within an application that separates resources from other resources that are used by that application.</span></span> <span data-ttu-id="2a791-127">Si existen grupos, asignaciones de funciones, definiciones de función o definiciones de tarea de Administrador de autorización que no desea implementar en toda una aplicación, puede crearlos en el nivel del ámbito.</span><span class="sxs-lookup"><span data-stu-id="2a791-127">If you have Authorization Manager groups, role assignments, role definitions, or task definitions that you do not want to apply to an entire application, you can create them at the scope level.</span></span>

## <a name="delegation"></a><span data-ttu-id="2a791-128">Delegación</span><span class="sxs-lookup"><span data-stu-id="2a791-128">Delegation</span></span>

<span data-ttu-id="2a791-129">Los almacenes de directivas de autorización que se almacenan en Active Directory admiten la delegación de la administración.</span><span class="sxs-lookup"><span data-stu-id="2a791-129">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="2a791-130">La administración se puede delegar a usuarios y grupos en el nivel de almacén, aplicación o ámbito.</span><span class="sxs-lookup"><span data-stu-id="2a791-130">Administration can be delegated to users and groups at the store, application, or scope level.</span></span> <span data-ttu-id="2a791-131">Cada nivel define roles administrativos para la Directiva en ese nivel.</span><span class="sxs-lookup"><span data-stu-id="2a791-131">Each level defines administrative roles for the policy at that level.</span></span> <span data-ttu-id="2a791-132">Para delegar el control a un usuario o grupo, asígnelos al rol de administrador; para permitir que un usuario o grupo Lea la Directiva, asígnela al rol lector.</span><span class="sxs-lookup"><span data-stu-id="2a791-132">To delegate control to a user or group, assign them to the administrator role; to allow a user or group to read the policy, assign them to the reader role.</span></span>

<span data-ttu-id="2a791-133">Los administradores de un almacén, aplicación o ámbito pueden leer y modificar el almacén de directivas en el nivel delegado.</span><span class="sxs-lookup"><span data-stu-id="2a791-133">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="2a791-134">Los lectores pueden leer el almacén de directivas en el nivel delegado, pero no pueden modificar el almacén.</span><span class="sxs-lookup"><span data-stu-id="2a791-134">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a791-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a791-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a791-136">Crear un objeto de almacén de directivas de autorización en C++</span><span class="sxs-lookup"><span data-stu-id="2a791-136">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="2a791-137">Crear un objeto de aplicación en C++</span><span class="sxs-lookup"><span data-stu-id="2a791-137">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="2a791-138">Delegación de la definición de permisos en C++</span><span class="sxs-lookup"><span data-stu-id="2a791-138">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



