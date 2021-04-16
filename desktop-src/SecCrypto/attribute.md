---
description: Representa un único atributo autenticado.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute, objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671631"
---
# <a name="attribute-object"></a><span data-ttu-id="3be22-103">Attribute, objeto</span><span class="sxs-lookup"><span data-stu-id="3be22-103">Attribute object</span></span>

<span data-ttu-id="3be22-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3be22-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="3be22-105">En su lugar, use la [**clase CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="3be22-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="3be22-106">El objeto de **atributo** representa un único atributo autenticado.</span><span class="sxs-lookup"><span data-stu-id="3be22-106">The **Attribute** object represents a single authenticated attribute.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="3be22-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="3be22-107">When to use</span></span>

<span data-ttu-id="3be22-108">El objeto de **atributo** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="3be22-108">The **Attribute** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="3be22-109">Establezca o recupere el nombre de CAPICOM del atributo.</span><span class="sxs-lookup"><span data-stu-id="3be22-109">Set or retrieve the CAPICOM name of the attribute.</span></span>
-   <span data-ttu-id="3be22-110">Establezca o recupere el valor del atributo, como la hora de la firma, el nombre del documento firmado o una descripción del documento firmado.</span><span class="sxs-lookup"><span data-stu-id="3be22-110">Set or retrieve the value of the attribute, such as signing time, the name of the document signed, or a description of the document signed.</span></span>

## <a name="members"></a><span data-ttu-id="3be22-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="3be22-111">Members</span></span>

<span data-ttu-id="3be22-112">El objeto de **atributo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3be22-112">The **Attribute** object has these types of members:</span></span>

-   [<span data-ttu-id="3be22-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3be22-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3be22-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3be22-114">Properties</span></span>

<span data-ttu-id="3be22-115">El objeto de **atributo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3be22-115">The **Attribute** object has these properties.</span></span>



| <span data-ttu-id="3be22-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3be22-116">Property</span></span>                                    | <span data-ttu-id="3be22-117">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="3be22-117">Access type</span></span>           | <span data-ttu-id="3be22-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3be22-118">Description</span></span>                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3be22-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="3be22-119">**Name**</span></span>](attribute-name.md)<br/>   | <span data-ttu-id="3be22-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3be22-120">Read/write</span></span><br/> | <span data-ttu-id="3be22-121">Establece o recupera el nombre de CAPICOM del atributo.</span><span class="sxs-lookup"><span data-stu-id="3be22-121">Sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="3be22-122">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3be22-122">This is the default property.</span></span><br/> |
| [<span data-ttu-id="3be22-123">**Value**</span><span class="sxs-lookup"><span data-stu-id="3be22-123">**Value**</span></span>](attribute-value.md)<br/> | <span data-ttu-id="3be22-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3be22-124">Read/write</span></span><br/> | <span data-ttu-id="3be22-125">Establece o recupera el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="3be22-125">Sets or retrieves the value of the attribute.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="3be22-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3be22-126">Remarks</span></span>

<span data-ttu-id="3be22-127">Se puede crear el objeto de **atributo** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="3be22-127">The **Attribute** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="3be22-128">El ProgID del objeto de **atributo** es CAPICOM. Attribute. 1.</span><span class="sxs-lookup"><span data-stu-id="3be22-128">The ProgID for the **Attribute** object is CAPICOM.Attribute.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be22-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3be22-129">Requirements</span></span>



| <span data-ttu-id="3be22-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3be22-130">Requirement</span></span> | <span data-ttu-id="3be22-131">Value</span><span class="sxs-lookup"><span data-stu-id="3be22-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3be22-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3be22-132">End of client support</span></span><br/> | <span data-ttu-id="3be22-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3be22-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3be22-134">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3be22-134">End of server support</span></span><br/> | <span data-ttu-id="3be22-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3be22-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3be22-136">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3be22-136">Redistributable</span></span><br/>       | <span data-ttu-id="3be22-137">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="3be22-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3be22-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3be22-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3be22-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3be22-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be22-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3be22-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be22-141">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="3be22-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
