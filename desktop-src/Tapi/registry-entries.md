---
description: Los terminales conectables se clasifican en superclases de terminal.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Entradas del registro (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689552"
---
# <a name="registry-entries-telephony-api"></a><span data-ttu-id="1f70d-103">Entradas del registro (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="1f70d-103">Registry Entries (Telephony API)</span></span>

<span data-ttu-id="1f70d-104">Los terminales conectables se clasifican en superclases de terminal.</span><span class="sxs-lookup"><span data-stu-id="1f70d-104">The pluggable terminals are classified into Terminal Superclasses.</span></span> <span data-ttu-id="1f70d-105">Cada superclase de terminal tiene una entrada en el registro con la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="1f70d-105">Each Terminal Superclass has an entry in the registry under the following key:</span></span>

<span data-ttu-id="1f70d-106">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Telephony** \\ **TerminalManager**</span><span class="sxs-lookup"><span data-stu-id="1f70d-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Telephony**\\**TerminalManager**</span></span>

<span data-ttu-id="1f70d-107">Debajo de la clave de la superclase de terminal hay entradas para cada terminal acoplable en la superclase de terminal.</span><span class="sxs-lookup"><span data-stu-id="1f70d-107">Below the Terminal Superclass key are entries for each pluggable terminal within the Terminal Superclass.</span></span>

<span data-ttu-id="1f70d-108">La entrada de cada superclase de terminal se identifica mediante un CLSID de la superclase de terminal.</span><span class="sxs-lookup"><span data-stu-id="1f70d-108">The entry for each Terminal Superclass is identified by a Terminal Superclass CLSID.</span></span> <span data-ttu-id="1f70d-109">Se trata de un identificador único para una clase de terminal.</span><span class="sxs-lookup"><span data-stu-id="1f70d-109">This is a unique identifier for a terminal class.</span></span> <span data-ttu-id="1f70d-110">La clase terminal tiene un atributo opcional: Name, que es un nombre descriptivo para la clase terminal.</span><span class="sxs-lookup"><span data-stu-id="1f70d-110">The terminal class has an optional attribute: name, which is a friendly name for the terminal class.</span></span> <span data-ttu-id="1f70d-111">Cada terminal acoplable se identifica mediante una clase terminal CLSID; es decir, un GUID.</span><span class="sxs-lookup"><span data-stu-id="1f70d-111">Each pluggable terminal is identified by a CLSID Terminal class; that is, a GUID.</span></span> <span data-ttu-id="1f70d-112">Los atributos del terminal acoplable se almacenan en valores de clave de terminal conectables.</span><span class="sxs-lookup"><span data-stu-id="1f70d-112">The attributes for pluggable terminal are stored into pluggable terminal key values.</span></span> <span data-ttu-id="1f70d-113">Los atributos de un terminal acoplable son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="1f70d-113">The attributes for a pluggable terminal are the following.</span></span>



| <span data-ttu-id="1f70d-114">Clase terminal</span><span class="sxs-lookup"><span data-stu-id="1f70d-114">Terminal class</span></span> | <span data-ttu-id="1f70d-115">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="1f70d-115">Key name</span></span> | <span data-ttu-id="1f70d-116">Identificador público</span><span class="sxs-lookup"><span data-stu-id="1f70d-116">Public identifier</span></span>                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1f70d-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f70d-117">Name</span></span>           | <span data-ttu-id="1f70d-118">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1f70d-118">REG\_SZ</span></span>  | <span data-ttu-id="1f70d-119">Nombre descriptivo del terminal</span><span class="sxs-lookup"><span data-stu-id="1f70d-119">Terminal friendly name</span></span>                                                            |
| <span data-ttu-id="1f70d-120">Compañía</span><span class="sxs-lookup"><span data-stu-id="1f70d-120">Company</span></span>        | <span data-ttu-id="1f70d-121">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1f70d-121">REG\_SZ</span></span>  | <span data-ttu-id="1f70d-122">Nombre de la compañía</span><span class="sxs-lookup"><span data-stu-id="1f70d-122">Company name</span></span>                                                                      |
| <span data-ttu-id="1f70d-123">Versión</span><span class="sxs-lookup"><span data-stu-id="1f70d-123">Version</span></span>        | <span data-ttu-id="1f70d-124">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1f70d-124">REG\_SZ</span></span>  | <span data-ttu-id="1f70d-125">Información de la versión</span><span class="sxs-lookup"><span data-stu-id="1f70d-125">Version information</span></span>                                                               |
| <span data-ttu-id="1f70d-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="1f70d-126">CLSID</span></span>          | <span data-ttu-id="1f70d-127">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1f70d-127">REG\_SZ</span></span>  | <span data-ttu-id="1f70d-128">Terminal CLSID (se usa en el método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) de com)</span><span class="sxs-lookup"><span data-stu-id="1f70d-128">Terminal CLSID (used in COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method)</span></span> |
| <span data-ttu-id="1f70d-129">Direcciones</span><span class="sxs-lookup"><span data-stu-id="1f70d-129">Directions</span></span>     | <span data-ttu-id="1f70d-130">DWORD</span><span class="sxs-lookup"><span data-stu-id="1f70d-130">DWORD</span></span>    | <span data-ttu-id="1f70d-131">Dirección del terminal</span><span class="sxs-lookup"><span data-stu-id="1f70d-131">Terminal direction</span></span>                                                                |
| <span data-ttu-id="1f70d-132">MediaTypes</span><span class="sxs-lookup"><span data-stu-id="1f70d-132">MediaTypes</span></span>     | <span data-ttu-id="1f70d-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="1f70d-133">DWORD</span></span>    | <span data-ttu-id="1f70d-134">Tipos de medios de terminal compatibles</span><span class="sxs-lookup"><span data-stu-id="1f70d-134">Terminal media types supported</span></span>                                                    |



 

<span data-ttu-id="1f70d-135">En el caso de una clase terminal, los atributos son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="1f70d-135">For a terminal class the attributes are the following.</span></span>



| <span data-ttu-id="1f70d-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="1f70d-136">CLSID</span></span> | <span data-ttu-id="1f70d-137">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="1f70d-137">Key name</span></span> | <span data-ttu-id="1f70d-138">Identificador público</span><span class="sxs-lookup"><span data-stu-id="1f70d-138">Public identifier</span></span>            |
|-------|----------|------------------------------|
| <span data-ttu-id="1f70d-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f70d-139">Name</span></span>  | <span data-ttu-id="1f70d-140">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1f70d-140">REG\_SZ</span></span>  | <span data-ttu-id="1f70d-141">Nombre descriptivo de la clase de terminal</span><span class="sxs-lookup"><span data-stu-id="1f70d-141">Terminal class friendly name</span></span> |



 

 

 
