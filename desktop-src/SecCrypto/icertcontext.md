---
description: Proporciona acceso al contexto de un objeto de certificado de CAPICOM X. 509v3. Este contexto permite usar el certificado de CAPICOM en otras derivaciones de CryptoAPI.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Interfaz ICertContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671619"
---
# <a name="icertcontext-interface"></a><span data-ttu-id="1e0bb-104">Interfaz ICertContext</span><span class="sxs-lookup"><span data-stu-id="1e0bb-104">ICertContext interface</span></span>

<span data-ttu-id="1e0bb-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="1e0bb-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="1e0bb-106">La interfaz **ICertContext** proporciona acceso al contexto de un objeto de [**certificado**](certificate.md) de CAPICOM X. 509v3.</span><span class="sxs-lookup"><span data-stu-id="1e0bb-106">The **ICertContext** interface provides access to the context of a CAPICOM X.509v3 [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="1e0bb-107">Este contexto permite usar el certificado de CAPICOM en otras derivaciones de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="1e0bb-107">This context allows the CAPICOM certificate to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="1e0bb-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="1e0bb-108">When to use</span></span>

<span data-ttu-id="1e0bb-109">Use esta interfaz cuando necesite usar un objeto de [**certificado**](certificate.md) de CAPICOM en otra derivación de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="1e0bb-109">Use this interface when you need to use a CAPICOM [**Certificate**](certificate.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="1e0bb-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e0bb-110">Members</span></span>

<span data-ttu-id="1e0bb-111">La interfaz **ICertContext** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1e0bb-111">The **ICertContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="1e0bb-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e0bb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1e0bb-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e0bb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1e0bb-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e0bb-114">Methods</span></span>

<span data-ttu-id="1e0bb-115">La interfaz **ICertContext** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1e0bb-115">The **ICertContext** interface has these methods.</span></span>



| <span data-ttu-id="1e0bb-116">Método</span><span class="sxs-lookup"><span data-stu-id="1e0bb-116">Method</span></span>                                          | <span data-ttu-id="1e0bb-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e0bb-117">Description</span></span>                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e0bb-118">**FreeContext**</span><span class="sxs-lookup"><span data-stu-id="1e0bb-118">**FreeContext**</span></span>](icertcontext-freecontext.md) | <span data-ttu-id="1e0bb-119">Libera un \_ contexto PCCERT adquirido a través de la propiedad [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="1e0bb-119">Releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1e0bb-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e0bb-120">Properties</span></span>

<span data-ttu-id="1e0bb-121">La interfaz **ICertContext** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1e0bb-121">The **ICertContext** interface has these properties.</span></span>



| <span data-ttu-id="1e0bb-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1e0bb-122">Property</span></span>                                                   | <span data-ttu-id="1e0bb-123">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="1e0bb-123">Access type</span></span>           | <span data-ttu-id="1e0bb-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e0bb-124">Description</span></span>                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="1e0bb-125">**CertContext**</span><span class="sxs-lookup"><span data-stu-id="1e0bb-125">**CertContext**</span></span>](icertcontext-certcontext.md)<br/> | <span data-ttu-id="1e0bb-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1e0bb-126">Read/write</span></span><br/> | <span data-ttu-id="1e0bb-127">Establece o recupera el contexto PCCERT \_ de un certificado.</span><span class="sxs-lookup"><span data-stu-id="1e0bb-127">Sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1e0bb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e0bb-128">Requirements</span></span>



| <span data-ttu-id="1e0bb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e0bb-129">Requirement</span></span> | <span data-ttu-id="1e0bb-130">Value</span><span class="sxs-lookup"><span data-stu-id="1e0bb-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0bb-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1e0bb-131">Redistributable</span></span><br/> | <span data-ttu-id="1e0bb-132">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bb-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1e0bb-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e0bb-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="1e0bb-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e0bb-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




