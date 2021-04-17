---
description: Proporciona acceso al contexto de un objeto de cadena CAPICOM. Este contexto permite usar la cadena de confianza de certificados de CAPICOM en otras derivaciones de CryptoAPI.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Interfaz IChainContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670297"
---
# <a name="ichaincontext-interface"></a><span data-ttu-id="f2b49-104">Interfaz IChainContext</span><span class="sxs-lookup"><span data-stu-id="f2b49-104">IChainContext interface</span></span>

<span data-ttu-id="f2b49-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="f2b49-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="f2b49-106">La interfaz **IChainContext** proporciona acceso al contexto de un objeto de [**cadena**](chain.md) CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="f2b49-106">The **IChainContext** interface provides access to the context of a CAPICOM [**Chain**](chain.md) object.</span></span> <span data-ttu-id="f2b49-107">Este contexto permite usar la cadena de confianza de certificados de CAPICOM en otras derivaciones de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="f2b49-107">This context allows the CAPICOM certificate trust chain to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f2b49-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="f2b49-108">When to use</span></span>

<span data-ttu-id="f2b49-109">Use esta interfaz cuando necesite usar un objeto de [**cadena**](chain.md) CAPICOM en otra derivación de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="f2b49-109">Use this interface when you need to use a CAPICOM [**Chain**](chain.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="f2b49-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f2b49-110">Members</span></span>

<span data-ttu-id="f2b49-111">La interfaz **IChainContext** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f2b49-111">The **IChainContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="f2b49-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f2b49-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f2b49-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2b49-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f2b49-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="f2b49-114">Methods</span></span>

<span data-ttu-id="f2b49-115">La interfaz **IChainContext** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f2b49-115">The **IChainContext** interface has these methods.</span></span>



| <span data-ttu-id="f2b49-116">Método</span><span class="sxs-lookup"><span data-stu-id="f2b49-116">Method</span></span>                                           | <span data-ttu-id="f2b49-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2b49-117">Description</span></span>                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2b49-118">**FreeContext**</span><span class="sxs-lookup"><span data-stu-id="f2b49-118">**FreeContext**</span></span>](ichaincontext-freecontext.md) | <span data-ttu-id="f2b49-119">Libera un \_ contexto de cadena PCCERT \_ adquirido a través de la propiedad [**ChainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="f2b49-119">Releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f2b49-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2b49-120">Properties</span></span>

<span data-ttu-id="f2b49-121">La interfaz **IChainContext** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f2b49-121">The **IChainContext** interface has these properties.</span></span>



| <span data-ttu-id="f2b49-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f2b49-122">Property</span></span>                                                      | <span data-ttu-id="f2b49-123">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f2b49-123">Access type</span></span>           | <span data-ttu-id="f2b49-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2b49-124">Description</span></span>                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="f2b49-125">**ChainContext**</span><span class="sxs-lookup"><span data-stu-id="f2b49-125">**ChainContext**</span></span>](ichaincontext-chaincontext.md)<br/> | <span data-ttu-id="f2b49-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2b49-126">Read/write</span></span><br/> | <span data-ttu-id="f2b49-127">Establece o recupera el \_ \_ contexto de la cadena de PCCERT de un certificado.</span><span class="sxs-lookup"><span data-stu-id="f2b49-127">Sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f2b49-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2b49-128">Requirements</span></span>



| <span data-ttu-id="f2b49-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2b49-129">Requirement</span></span> | <span data-ttu-id="f2b49-130">Value</span><span class="sxs-lookup"><span data-stu-id="f2b49-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b49-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f2b49-131">Redistributable</span></span><br/> | <span data-ttu-id="f2b49-132">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="f2b49-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f2b49-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2b49-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="f2b49-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2b49-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




