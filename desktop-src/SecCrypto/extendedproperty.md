---
description: Representa una propiedad extendida de Microsoft.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: Objeto ExtendedProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671041"
---
# <a name="extendedproperty-object"></a><span data-ttu-id="83680-103">Objeto ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="83680-103">ExtendedProperty object</span></span>

<span data-ttu-id="83680-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="83680-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="83680-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a la función de la API de Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="83680-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="83680-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="83680-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="83680-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="83680-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="83680-108">El objeto **ExtendedProperty** representa una propiedad extendida de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="83680-108">The **ExtendedProperty** object represents a Microsoft-extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="83680-109">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="83680-109">When to use</span></span>

<span data-ttu-id="83680-110">El objeto **ExtendedProperty** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="83680-110">The **ExtendedProperty** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="83680-111">Establezca o recupere el tipo de la propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="83680-111">Set or retrieve the type of the extended property.</span></span>
-   <span data-ttu-id="83680-112">Establece o recupera el tipo de codificación utilizado para codificar la propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="83680-112">Set or retrieve the type of encoding used to encode the extended property.</span></span>

## <a name="members"></a><span data-ttu-id="83680-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="83680-113">Members</span></span>

<span data-ttu-id="83680-114">El objeto **ExtendedProperty** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="83680-114">The **ExtendedProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="83680-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83680-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83680-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83680-116">Properties</span></span>

<span data-ttu-id="83680-117">El objeto **ExtendedProperty** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="83680-117">The **ExtendedProperty** object has these properties.</span></span>



| <span data-ttu-id="83680-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="83680-118">Property</span></span>                                             | <span data-ttu-id="83680-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="83680-119">Access type</span></span>           | <span data-ttu-id="83680-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="83680-120">Description</span></span>                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83680-121">**PropID**</span><span class="sxs-lookup"><span data-stu-id="83680-121">**PropID**</span></span>](extendedproperty-propid.md)<br/> | <span data-ttu-id="83680-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="83680-122">Read/write</span></span><br/> | <span data-ttu-id="83680-123">Un valor de la enumeración de [**CAPICOM \_ PROPID**](capicom-propid.md) que establece o recupera el tipo de propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="83680-123">A value of the [**CAPICOM\_PROPID**](capicom-propid.md) enumeration that sets or retrieves the type of extended property.</span></span><br/> <span data-ttu-id="83680-124">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="83680-124">This is the default property.</span></span><br/> |
| [<span data-ttu-id="83680-125">**Value**</span><span class="sxs-lookup"><span data-stu-id="83680-125">**Value**</span></span>](extendedproperty-value.md)<br/>   | <span data-ttu-id="83680-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="83680-126">Read/write</span></span><br/> | <span data-ttu-id="83680-127">Un valor de la enumeración de [**\_ \_ tipo de codificación CAPICOM**](capicom-encoding-type.md) que establece o recupera los datos de la propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="83680-127">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that sets or retrieves the extended property data.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="83680-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83680-128">Remarks</span></span>

<span data-ttu-id="83680-129">La colección [**ExtendedProperties**](extendedproperties.md) usa el objeto **ExtendedProperty** .</span><span class="sxs-lookup"><span data-stu-id="83680-129">The **ExtendedProperty** object is used by the [**ExtendedProperties**](extendedproperties.md) collection.</span></span>

<span data-ttu-id="83680-130">Se puede crear el objeto **ExtendedProperty** y no es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="83680-130">The **ExtendedProperty** object can be created, and it is not safe for scripting.</span></span> <span data-ttu-id="83680-131">El ProgID del objeto **ExtendedProperty** es CAPICOM. ExtendedProperty. 1.</span><span class="sxs-lookup"><span data-stu-id="83680-131">The ProgID for the **ExtendedProperty** object is CAPICOM.ExtendedProperty.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="83680-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83680-132">Requirements</span></span>



| <span data-ttu-id="83680-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="83680-133">Requirement</span></span> | <span data-ttu-id="83680-134">Value</span><span class="sxs-lookup"><span data-stu-id="83680-134">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83680-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="83680-135">End of client support</span></span><br/> | <span data-ttu-id="83680-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83680-136">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="83680-137">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="83680-137">End of server support</span></span><br/> | <span data-ttu-id="83680-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83680-138">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="83680-139">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="83680-139">Redistributable</span></span><br/>       | <span data-ttu-id="83680-140">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="83680-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="83680-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="83680-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="83680-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83680-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
