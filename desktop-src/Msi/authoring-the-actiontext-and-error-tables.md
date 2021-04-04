---
description: Las especificaciones de ejemplo incluyen el envío de mensajes de ActionData cuando una acción personalizada crea o quita una cuenta de usuario y notifica un error si no se puede crear una cuenta.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Creación de las tablas de error y de ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909070"
---
# <a name="authoring-the-actiontext-and-error-tables"></a><span data-ttu-id="fde44-103">Creación de las tablas de error y de ActionText</span><span class="sxs-lookup"><span data-stu-id="fde44-103">Authoring the ActionText and Error Tables</span></span>

<span data-ttu-id="fde44-104">Las especificaciones de ejemplo incluyen el envío de mensajes de ActionData cuando una acción personalizada crea o quita una cuenta de usuario y notifica un error si no se puede crear una cuenta.</span><span class="sxs-lookup"><span data-stu-id="fde44-104">The sample specifications include sending ActionData messages when a custom action creates or removes a user account, and reporting an error if an account cannot be created.</span></span>

<span data-ttu-id="fde44-105">Escriba las siguientes entradas en la tabla de ActionText para proporcionar información usada por los mensajes de ActionText.</span><span class="sxs-lookup"><span data-stu-id="fde44-105">Enter the following entries into the ActionText table to provide information used by ActionText messages.</span></span>

[<span data-ttu-id="fde44-106">Tabla de ActionText</span><span class="sxs-lookup"><span data-stu-id="fde44-106">ActionText Table</span></span>](actiontext-table.md)



| <span data-ttu-id="fde44-107">Acción</span><span class="sxs-lookup"><span data-stu-id="fde44-107">Action</span></span>            | <span data-ttu-id="fde44-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fde44-108">Description</span></span>                                                       | <span data-ttu-id="fde44-109">Plantilla</span><span class="sxs-lookup"><span data-stu-id="fde44-109">Template</span></span>                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="fde44-110">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="fde44-110">ProcessAccounts</span></span>   | <span data-ttu-id="fde44-111">Generar acciones para crear cuentas de usuario en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="fde44-111">Generating actions to create user accounts on the local computer.</span></span> | <span data-ttu-id="fde44-112">Cuenta: \[ 1 \] , atributos: \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="fde44-112">Account: \[1\], Attributes: \[2\]</span></span> |
| <span data-ttu-id="fde44-113">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="fde44-113">CreateAccount</span></span>     | <span data-ttu-id="fde44-114">Creando una cuenta de usuario en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="fde44-114">Creating user account on the local computer.</span></span>                      | <span data-ttu-id="fde44-115">Cuenta: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="fde44-115">Account: \[1\]</span></span>                    |
| <span data-ttu-id="fde44-116">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="fde44-116">RemoveAccount</span></span>     | <span data-ttu-id="fde44-117">Quitando la cuenta de usuario del equipo local.</span><span class="sxs-lookup"><span data-stu-id="fde44-117">Removing user account from the local computer.</span></span>                    | <span data-ttu-id="fde44-118">Cuenta: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="fde44-118">Account: \[1\]</span></span>                    |
| <span data-ttu-id="fde44-119">RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="fde44-119">RollbackAccount</span></span>   | <span data-ttu-id="fde44-120">Revertir la creación de cuentas de usuario en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="fde44-120">Rolling back the creation of user accounts on the local computer.</span></span> | <span data-ttu-id="fde44-121">Cuenta: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="fde44-121">Account: \[1\]</span></span>                    |
| <span data-ttu-id="fde44-122">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="fde44-122">UninstallAccounts</span></span> | <span data-ttu-id="fde44-123">Generar acciones para quitar cuentas de usuario en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="fde44-123">Generating actions to remove user accounts on the local computer.</span></span> | <span data-ttu-id="fde44-124">Cuenta: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="fde44-124">Account: \[1\]</span></span>                    |



 

<span data-ttu-id="fde44-125">Escriba las siguientes entradas en la tabla de errores para proporcionar la información que utiliza el informe de errores.</span><span class="sxs-lookup"><span data-stu-id="fde44-125">Enter the following entries into the Error table to provide information used by error reporting.</span></span>

[<span data-ttu-id="fde44-126">Tabla de errores</span><span class="sxs-lookup"><span data-stu-id="fde44-126">Error Table</span></span>](error-table.md)



| <span data-ttu-id="fde44-127">Error</span><span class="sxs-lookup"><span data-stu-id="fde44-127">Error</span></span> | <span data-ttu-id="fde44-128">Message</span><span class="sxs-lookup"><span data-stu-id="fde44-128">Message</span></span>                                                                        |
|-------|--------------------------------------------------------------------------------|
| <span data-ttu-id="fde44-129">25001</span><span class="sxs-lookup"><span data-stu-id="fde44-129">25001</span></span> | <span data-ttu-id="fde44-130">No se puede crear la cuenta \[ de usuario ' 2 \] ' en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="fde44-130">Unable to create user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="fde44-131">Código de error: \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="fde44-131">Error Code: \[3\].</span></span> |
| <span data-ttu-id="fde44-132">25002</span><span class="sxs-lookup"><span data-stu-id="fde44-132">25002</span></span> | <span data-ttu-id="fde44-133">La cuenta de usuario ' \[ 2 \] ' ya existe en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="fde44-133">User account '\[2\]' already exists on the local machine.</span></span>                      |
| <span data-ttu-id="fde44-134">25003</span><span class="sxs-lookup"><span data-stu-id="fde44-134">25003</span></span> | <span data-ttu-id="fde44-135">No se puede quitar la cuenta \[ de usuario ' 2 \] ' en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="fde44-135">Unable to remove user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="fde44-136">Código de error: \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="fde44-136">Error Code: \[3\].</span></span> |
| <span data-ttu-id="fde44-137">25004</span><span class="sxs-lookup"><span data-stu-id="fde44-137">25004</span></span> | <span data-ttu-id="fde44-138">La cuenta de usuario ' \[ 2 \] ' no existe en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="fde44-138">User account '\[2\]' does not exist on the local machine.</span></span>                      |



 

<span data-ttu-id="fde44-139">Continúe con [la creación de la tabla InstallExecuteSequence](authoring-the-installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="fde44-139">Continue to [Authoring the InstallExecuteSequence Table](authoring-the-installexecutesequence-table.md).</span></span>

 

 



