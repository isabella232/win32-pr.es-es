---
description: Proporciona funcionalidad para la generación de números aleatorios, las conversiones y la codificación y descodificación de Base64.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Objeto Utilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671403"
---
# <a name="utilities-object"></a><span data-ttu-id="19773-103">Objeto Utilities</span><span class="sxs-lookup"><span data-stu-id="19773-103">Utilities object</span></span>

<span data-ttu-id="19773-104">\[El objeto **Utilities** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="19773-104">\[The **Utilities** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="19773-105">El objeto **Utilities** proporciona funcionalidad para la generación de números aleatorios, las conversiones y la codificación y descodificación de Base64.</span><span class="sxs-lookup"><span data-stu-id="19773-105">The **Utilities** object provides functionality for random number generation, conversions, and encoding and decoding from base64.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="19773-106">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="19773-106">When to use</span></span>

<span data-ttu-id="19773-107">El objeto **Utilities** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="19773-107">The **Utilities** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="19773-108">Codifique una cadena como base64 o descodifique una cadena de Base64.</span><span class="sxs-lookup"><span data-stu-id="19773-108">Encode a string as base64 or decode a string from base64.</span></span>
-   <span data-ttu-id="19773-109">Convierte una cadena empaquetada en binaria en una matriz de bytes y viceversa.</span><span class="sxs-lookup"><span data-stu-id="19773-109">Convert a binary-packed string to a byte array and vice versa.</span></span>
-   <span data-ttu-id="19773-110">Convierte una cadena empaquetada en binaria en una cadena hexadecimal y viceversa.</span><span class="sxs-lookup"><span data-stu-id="19773-110">Convert a binary-packed string to a hexadecimal string and vice versa.</span></span>
-   <span data-ttu-id="19773-111">Generar un número aleatorio seguro.</span><span class="sxs-lookup"><span data-stu-id="19773-111">Generate a secure random number.</span></span>
-   <span data-ttu-id="19773-112">Convertir la hora local en hora universal coordinada (hora del meridiano de Greenwich) y viceversa.</span><span class="sxs-lookup"><span data-stu-id="19773-112">Convert local time to Coordinated Universal Time (Greenwich Mean Time) and vice versa.</span></span>

## <a name="members"></a><span data-ttu-id="19773-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="19773-113">Members</span></span>

<span data-ttu-id="19773-114">El objeto **Utilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="19773-114">The **Utilities** object has these types of members:</span></span>

-   [<span data-ttu-id="19773-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="19773-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="19773-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="19773-116">Methods</span></span>

<span data-ttu-id="19773-117">El objeto **Utilities** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="19773-117">The **Utilities** object has these methods.</span></span>



| <span data-ttu-id="19773-118">Método</span><span class="sxs-lookup"><span data-stu-id="19773-118">Method</span></span>                                                               | <span data-ttu-id="19773-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="19773-119">Description</span></span>                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="19773-120">**Base64Decode**</span><span class="sxs-lookup"><span data-stu-id="19773-120">**Base64Decode**</span></span>](utilities-base64decode.md)                       | <span data-ttu-id="19773-121">Descodifica una cadena de Base64.</span><span class="sxs-lookup"><span data-stu-id="19773-121">Decodes a string from base64.</span></span><br/>                                     |
| [<span data-ttu-id="19773-122">**Base64Encode**</span><span class="sxs-lookup"><span data-stu-id="19773-122">**Base64Encode**</span></span>](utilities-base64encode.md)                       | <span data-ttu-id="19773-123">Codifica una cadena como Base64.</span><span class="sxs-lookup"><span data-stu-id="19773-123">Encodes a string as base64.</span></span><br/>                                       |
| [<span data-ttu-id="19773-124">**BinaryStringToByteArray**</span><span class="sxs-lookup"><span data-stu-id="19773-124">**BinaryStringToByteArray**</span></span>](utilities-binarystringtobytearray.md) | <span data-ttu-id="19773-125">Convierte una cadena empaquetada en binaria en una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="19773-125">Converts a binary-packed string to an array of bytes.</span></span><br/>             |
| [<span data-ttu-id="19773-126">**BinaryToHex**</span><span class="sxs-lookup"><span data-stu-id="19773-126">**BinaryToHex**</span></span>](utilities-binarytohex.md)                         | <span data-ttu-id="19773-127">Convierte una cadena empaquetada en binaria en una cadena hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="19773-127">Converts a binary-packed string to a hexadecimal string.</span></span><br/>          |
| [<span data-ttu-id="19773-128">**ByteArrayToBinaryString**</span><span class="sxs-lookup"><span data-stu-id="19773-128">**ByteArrayToBinaryString**</span></span>](utilities-bytearraytobinarystring.md) | <span data-ttu-id="19773-129">Convierte una matriz de bytes en una cadena empaquetada como binaria.</span><span class="sxs-lookup"><span data-stu-id="19773-129">Converts an array of bytes to a binary-packed string.</span></span><br/>             |
| [<span data-ttu-id="19773-130">**GetRandom**</span><span class="sxs-lookup"><span data-stu-id="19773-130">**GetRandom**</span></span>](utilities-getrandom.md)                             | <span data-ttu-id="19773-131">Genera un número aleatorio seguro.</span><span class="sxs-lookup"><span data-stu-id="19773-131">Generates a secure random number.</span></span><br/>                                 |
| [<span data-ttu-id="19773-132">**HexToBinary**</span><span class="sxs-lookup"><span data-stu-id="19773-132">**HexToBinary**</span></span>](utilities-hextobinary.md)                         | <span data-ttu-id="19773-133">Convierte una cadena hexadecimal en una cadena empaquetada como binaria.</span><span class="sxs-lookup"><span data-stu-id="19773-133">Converts a hexadecimal string to a binary-packed string.</span></span><br/>          |
| [<span data-ttu-id="19773-134">**LocalTimeToUTCTime**</span><span class="sxs-lookup"><span data-stu-id="19773-134">**LocalTimeToUTCTime**</span></span>](utilities-localtimetoutctime.md)           | <span data-ttu-id="19773-135">Convierte la hora local del equipo en hora universal coordinada.</span><span class="sxs-lookup"><span data-stu-id="19773-135">Converts the computer's local time to Coordinated Universal Time.</span></span><br/> |
| [<span data-ttu-id="19773-136">**UTCTimeToLocalTime**</span><span class="sxs-lookup"><span data-stu-id="19773-136">**UTCTimeToLocalTime**</span></span>](utilities-utctimetolocaltime.md)           | <span data-ttu-id="19773-137">Convierte la hora universal coordinada en la hora local del equipo.</span><span class="sxs-lookup"><span data-stu-id="19773-137">Converts Coordinated Universal Time to the computer's local time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="19773-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19773-138">Remarks</span></span>

<span data-ttu-id="19773-139">Se puede crear el objeto **Utilities** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="19773-139">The **Utilities** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="19773-140">El ProgID del objeto **Utilities** es CAPICOM. Utilities. 1.</span><span class="sxs-lookup"><span data-stu-id="19773-140">The ProgID for the **Utilities** object is CAPICOM.Utilities.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="19773-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19773-141">Requirements</span></span>



| <span data-ttu-id="19773-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="19773-142">Requirement</span></span> | <span data-ttu-id="19773-143">Value</span><span class="sxs-lookup"><span data-stu-id="19773-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19773-144">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="19773-144">Redistributable</span></span><br/> | <span data-ttu-id="19773-145">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="19773-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="19773-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="19773-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="19773-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19773-147"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




