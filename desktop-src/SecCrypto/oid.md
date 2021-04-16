---
description: Representa un identificador de objeto (OID) que se usa en varias propiedades de CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: Objeto OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671786"
---
# <a name="oid-object"></a><span data-ttu-id="7e7cf-103">Objeto OID</span><span class="sxs-lookup"><span data-stu-id="7e7cf-103">OID object</span></span>

<span data-ttu-id="7e7cf-104">\[El objeto **OID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-104">\[The **OID** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7e7cf-105">En su lugar, use la [**clase OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="7e7cf-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7e7cf-106">El objeto **OID** representa un [*identificador de objeto*](../secgloss/o-gly.md) (OID) que se usa en varias propiedades de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-106">The **OID** object represents an [*object identifier*](../secgloss/o-gly.md) (OID) that is used by several CAPICOM properties.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7e7cf-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="7e7cf-107">When to use</span></span>

<span data-ttu-id="7e7cf-108">El objeto **OID** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="7e7cf-108">The **OID** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="7e7cf-109">Establezca o recupere un nombre de CAPICOM y un nombre para mostrar para el OID.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-109">Set or retrieve a CAPICOM name and display name for the OID.</span></span>
-   <span data-ttu-id="7e7cf-110">Establece o recupera el número de puntos del OID.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-110">Set or retrieve the dotted number for the OID.</span></span>

## <a name="members"></a><span data-ttu-id="7e7cf-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e7cf-111">Members</span></span>

<span data-ttu-id="7e7cf-112">El objeto **OID** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7e7cf-112">The **OID** object has these types of members:</span></span>

-   [<span data-ttu-id="7e7cf-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e7cf-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e7cf-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e7cf-114">Properties</span></span>

<span data-ttu-id="7e7cf-115">El objeto **OID** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-115">The **OID** object has these properties.</span></span>



| <span data-ttu-id="7e7cf-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7e7cf-116">Property</span></span>                                            | <span data-ttu-id="7e7cf-117">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="7e7cf-117">Access type</span></span>           | <span data-ttu-id="7e7cf-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e7cf-118">Description</span></span>                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e7cf-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="7e7cf-119">**FriendlyName**</span></span>](oid-friendlyname.md)<br/> | <span data-ttu-id="7e7cf-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e7cf-120">Read/write</span></span><br/> | <span data-ttu-id="7e7cf-121">Establece o recupera el nombre para mostrar del OID.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-121">Sets or retrieves the display name for the OID.</span></span><br/>                                       |
| [<span data-ttu-id="7e7cf-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="7e7cf-122">**Name**</span></span>](oid-name.md)<br/>                 | <span data-ttu-id="7e7cf-123">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e7cf-123">Read/write</span></span><br/> | <span data-ttu-id="7e7cf-124">Establece o recupera el nombre definido por CAPICOM para el OID.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-124">Sets or retrieves the CAPICOM-defined name for the OID.</span></span> <span data-ttu-id="7e7cf-125">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-125">This is the default property.</span></span><br/> |
| [<span data-ttu-id="7e7cf-126">**Value**</span><span class="sxs-lookup"><span data-stu-id="7e7cf-126">**Value**</span></span>](oid-value.md)<br/>               | <span data-ttu-id="7e7cf-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e7cf-127">Read/write</span></span><br/> | <span data-ttu-id="7e7cf-128">Establece o recupera el valor del número de puntos OID del OID.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-128">Sets or retrieves the value of the OID dotted number of the OID.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="7e7cf-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e7cf-129">Remarks</span></span>

<span data-ttu-id="7e7cf-130">Se puede crear el objeto **OID** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-130">The **OID** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="7e7cf-131">El ProgID del objeto **OID** es CAPICOM. OID. 1.</span><span class="sxs-lookup"><span data-stu-id="7e7cf-131">The ProgID for the **OID** object is CAPICOM.OID.1.</span></span>

<span data-ttu-id="7e7cf-132">Las siguientes propiedades de objeto de CAPICOM devuelven un objeto **OID** :</span><span class="sxs-lookup"><span data-stu-id="7e7cf-132">The following CAPICOM object properties return an **OID** object:</span></span>

-   [<span data-ttu-id="7e7cf-133">**PolicyInformation. OID**</span><span class="sxs-lookup"><span data-stu-id="7e7cf-133">**PolicyInformation.OID**</span></span>](policyinformation-oid.md)
-   [<span data-ttu-id="7e7cf-134">**Calificador. OID**</span><span class="sxs-lookup"><span data-stu-id="7e7cf-134">**Qualifier.OID**</span></span>](qualifier-oid.md)
-   [<span data-ttu-id="7e7cf-135">**Extensión. OID**</span><span class="sxs-lookup"><span data-stu-id="7e7cf-135">**Extension.OID**</span></span>](extension-oid.md)
-   [<span data-ttu-id="7e7cf-136">**Plantilla. OID**</span><span class="sxs-lookup"><span data-stu-id="7e7cf-136">**Template.OID**</span></span>](template-oid.md)

## <a name="requirements"></a><span data-ttu-id="7e7cf-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e7cf-137">Requirements</span></span>



| <span data-ttu-id="7e7cf-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e7cf-138">Requirement</span></span> | <span data-ttu-id="7e7cf-139">Value</span><span class="sxs-lookup"><span data-stu-id="7e7cf-139">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7cf-140">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7e7cf-140">Redistributable</span></span><br/> | <span data-ttu-id="7e7cf-141">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7e7cf-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7e7cf-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e7cf-142">DLL</span></span><br/>             | <dl> <span data-ttu-id="7e7cf-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e7cf-143"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
