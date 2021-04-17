---
description: Proporciona acceso al contexto de un objeto de almacén de CAPICOM. Este contexto permite usar el almacén de certificados de CAPICOM en otras derivaciones de CryptoAPI.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Interfaz ICertStore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690475"
---
# <a name="icertstore-interface"></a><span data-ttu-id="7c75f-104">Interfaz ICertStore</span><span class="sxs-lookup"><span data-stu-id="7c75f-104">ICertStore interface</span></span>

<span data-ttu-id="7c75f-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="7c75f-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="7c75f-106">La interfaz **ICertStore** proporciona acceso al contexto de un objeto de [**almacén**](store.md) de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="7c75f-106">The **ICertStore** interface provides access to the context of a CAPICOM [**Store**](store.md) object.</span></span> <span data-ttu-id="7c75f-107">Este contexto permite usar el almacén de certificados de CAPICOM en otras derivaciones de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="7c75f-107">This context allows the CAPICOM certificate store to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7c75f-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="7c75f-108">When to use</span></span>

<span data-ttu-id="7c75f-109">Use esta interfaz cuando necesite usar un objeto de [**almacén**](store.md) de CAPICOM en otra derivación de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="7c75f-109">Use this interface when you need to use a CAPICOM [**Store**](store.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="7c75f-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="7c75f-110">Members</span></span>

<span data-ttu-id="7c75f-111">La interfaz **ICertStore** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7c75f-111">The **ICertStore** interface has these types of members:</span></span>

-   [<span data-ttu-id="7c75f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="7c75f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7c75f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c75f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7c75f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="7c75f-114">Methods</span></span>

<span data-ttu-id="7c75f-115">La interfaz **ICertStore** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7c75f-115">The **ICertStore** interface has these methods.</span></span>



| <span data-ttu-id="7c75f-116">Método</span><span class="sxs-lookup"><span data-stu-id="7c75f-116">Method</span></span>                                        | <span data-ttu-id="7c75f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c75f-117">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c75f-118">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="7c75f-118">**CloseHandle**</span></span>](icertstore-closehandle.md) | <span data-ttu-id="7c75f-119">Cierra un identificador HCERTSTORE adquirido a través de la propiedad [**StoreHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="7c75f-119">Closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7c75f-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c75f-120">Properties</span></span>

<span data-ttu-id="7c75f-121">La interfaz **ICertStore** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7c75f-121">The **ICertStore** interface has these properties.</span></span>



| <span data-ttu-id="7c75f-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c75f-122">Property</span></span>                                                     | <span data-ttu-id="7c75f-123">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="7c75f-123">Access type</span></span>           | <span data-ttu-id="7c75f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c75f-124">Description</span></span>                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c75f-125">**StoreHandle**</span><span class="sxs-lookup"><span data-stu-id="7c75f-125">**StoreHandle**</span></span>](icertstore-storehandle.md)<br/>     | <span data-ttu-id="7c75f-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7c75f-126">Read/write</span></span><br/> | <span data-ttu-id="7c75f-127">Establece o recupera el identificador HCERTSTORE de un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="7c75f-127">Sets or retrieves the HCERTSTORE handle of a certificate store.</span></span><br/>                                          |
| [<span data-ttu-id="7c75f-128">**StoreLocation**</span><span class="sxs-lookup"><span data-stu-id="7c75f-128">**StoreLocation**</span></span>](icertstore-storelocation.md)<br/> | <span data-ttu-id="7c75f-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7c75f-129">Read/write</span></span><br/> | <span data-ttu-id="7c75f-130">Establece o recupera la [**Ubicación del \_ almacén \_ de CAPICOM**](capicom-store-location.md) de un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="7c75f-130">Sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7c75f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c75f-131">Requirements</span></span>



| <span data-ttu-id="7c75f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c75f-132">Requirement</span></span> | <span data-ttu-id="7c75f-133">Value</span><span class="sxs-lookup"><span data-stu-id="7c75f-133">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c75f-134">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7c75f-134">Redistributable</span></span><br/> | <span data-ttu-id="7c75f-135">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c75f-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7c75f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c75f-136">DLL</span></span><br/>             | <dl> <span data-ttu-id="7c75f-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c75f-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




