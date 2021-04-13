---
title: OP_PACKAGE_PART
description: Definición de OP_PACKAGE_PART IDL
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104271915"
---
# <a name="op_package_part-structure"></a><span data-ttu-id="52b3d-103">Estructura de OP_PACKAGE_PART</span><span class="sxs-lookup"><span data-stu-id="52b3d-103">OP_PACKAGE_PART structure</span></span>

<span data-ttu-id="52b3d-104">Define una estructura que contiene un conjunto de datos identificado por un GUID.</span><span class="sxs-lookup"><span data-stu-id="52b3d-104">Defines a structure that contains a data set identified by a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="52b3d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52b3d-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a><span data-ttu-id="52b3d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="52b3d-106">Members</span></span>

### <a name="parttype"></a><span data-ttu-id="52b3d-107">PartType</span><span class="sxs-lookup"><span data-stu-id="52b3d-107">PartType</span></span>

<span data-ttu-id="52b3d-108">Identifica la estructura serializada incluida en la parte de la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="52b3d-108">Identifies the serialized structure contained in Part per the following table:</span></span>

|<span data-ttu-id="52b3d-109">PartType</span><span class="sxs-lookup"><span data-stu-id="52b3d-109">PartType</span></span>|<span data-ttu-id="52b3d-110">Significado</span><span class="sxs-lookup"><span data-stu-id="52b3d-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="52b3d-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span><span class="sxs-lookup"><span data-stu-id="52b3d-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span></span>|<span data-ttu-id="52b3d-112">Contiene una estructura de ODJ_WIN7_BLOB serializada.</span><span class="sxs-lookup"><span data-stu-id="52b3d-112">Contains a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="52b3d-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span><span class="sxs-lookup"><span data-stu-id="52b3d-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span></span>|<span data-ttu-id="52b3d-114">Contiene una estructura de OP_JOIN_PROV2_PART serializada.</span><span class="sxs-lookup"><span data-stu-id="52b3d-114">Contains a serialized OP_JOIN_PROV2_PART structure.</span></span>|
|<span data-ttu-id="52b3d-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span><span class="sxs-lookup"><span data-stu-id="52b3d-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span></span>|<span data-ttu-id="52b3d-116">Contiene una estructura de OP_JOIN_PROV3_PART serializada.</span><span class="sxs-lookup"><span data-stu-id="52b3d-116">Contains a serialized OP_JOIN_PROV3_PART structure.</span></span>|
|<span data-ttu-id="52b3d-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span><span class="sxs-lookup"><span data-stu-id="52b3d-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span></span>|<span data-ttu-id="52b3d-118">Contiene una estructura de OP_CERT_PART serializada.</span><span class="sxs-lookup"><span data-stu-id="52b3d-118">Contains a serialized OP_CERT_PART structure.</span></span>|
|<span data-ttu-id="52b3d-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span><span class="sxs-lookup"><span data-stu-id="52b3d-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span></span>|<span data-ttu-id="52b3d-120">Contiene una estructura de OP_POLICY_PART serializada.</span><span class="sxs-lookup"><span data-stu-id="52b3d-120">Contains a serialized OP_POLICY_PART structure.</span></span>|

### <a name="ulflags"></a><span data-ttu-id="52b3d-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="52b3d-121">ulFlags</span></span>

<span data-ttu-id="52b3d-122">Debe establecerse en cero o más de los siguientes marcadores:</span><span class="sxs-lookup"><span data-stu-id="52b3d-122">Must be set to zero or more of the following flags:</span></span>

|<span data-ttu-id="52b3d-123">Value</span><span class="sxs-lookup"><span data-stu-id="52b3d-123">Value</span></span>|<span data-ttu-id="52b3d-124">Significado</span><span class="sxs-lookup"><span data-stu-id="52b3d-124">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="52b3d-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="52b3d-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span></span>|<span data-ttu-id="52b3d-126">Este componente del paquete se considera esencial.</span><span class="sxs-lookup"><span data-stu-id="52b3d-126">This package part is considered essential.</span></span> <span data-ttu-id="52b3d-127">Si el consumidor no reconoce este componente del paquete o no lo procesa correctamente, se debe producir un error en la operación global.</span><span class="sxs-lookup"><span data-stu-id="52b3d-127">If the consumer does not recognize this package part or fails to successfully process it, the overall operation must fail.</span></span>|

### <a name="part"></a><span data-ttu-id="52b3d-128">Parte</span><span class="sxs-lookup"><span data-stu-id="52b3d-128">Part</span></span>

<span data-ttu-id="52b3d-129">Contiene una estructura serializada en una estructura de OP_BLOB.</span><span class="sxs-lookup"><span data-stu-id="52b3d-129">Contains a serialized structure in an OP_BLOB structure.</span></span> <span data-ttu-id="52b3d-130">La estructura específica viene determinada por PartType.</span><span class="sxs-lookup"><span data-stu-id="52b3d-130">The specific structure is determined by PartType.</span></span>

### <a name="extension"></a><span data-ttu-id="52b3d-131">Extensión</span><span class="sxs-lookup"><span data-stu-id="52b3d-131">Extension</span></span>

<span data-ttu-id="52b3d-132">Reservado para uso futuro y debe establecerse en ceros.</span><span class="sxs-lookup"><span data-stu-id="52b3d-132">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="52b3d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="52b3d-133">See also</span></span>

[<span data-ttu-id="52b3d-134">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="52b3d-134">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="52b3d-135">**BLOB de operaciones \_**</span><span class="sxs-lookup"><span data-stu-id="52b3d-135">**OP\_BLOB**</span></span>](odj-op_blob.md)
