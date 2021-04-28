---
description: 'Interfaz IEnumPStoreTypes: proporciona métodos de enumeración com estándar para la interfaz IPStore.'
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Interfaz IEnumPStoreTypes (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7ca2e250864889a5fda465e146287bf59a2b6346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089363"
---
# <a name="ienumpstoretypes-interface"></a><span data-ttu-id="b26da-103">IEnumPStoreTypes (interfaz)</span><span class="sxs-lookup"><span data-stu-id="b26da-103">IEnumPStoreTypes interface</span></span>

<span data-ttu-id="b26da-104">\[El almacenamiento protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b26da-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b26da-105">Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b26da-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b26da-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="b26da-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b26da-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="b26da-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b26da-108">Proporciona métodos de enumeración com estándar para la [**interfaz IPStore.**](ipstore.md)</span><span class="sxs-lookup"><span data-stu-id="b26da-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="b26da-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b26da-109">Members</span></span>

<span data-ttu-id="b26da-110">La **interfaz IEnumPStoreTypes** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="b26da-110">The **IEnumPStoreTypes** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b26da-111">**IEnumPStoreTypes también** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b26da-111">**IEnumPStoreTypes** also has these types of members:</span></span>

-   [<span data-ttu-id="b26da-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b26da-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b26da-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="b26da-113">Methods</span></span>

<span data-ttu-id="b26da-114">La **interfaz IEnumPStoreTypes** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b26da-114">The **IEnumPStoreTypes** interface has these methods.</span></span>



| <span data-ttu-id="b26da-115">Método</span><span class="sxs-lookup"><span data-stu-id="b26da-115">Method</span></span>                                  | <span data-ttu-id="b26da-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b26da-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b26da-117">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="b26da-117">**Clone**</span></span>](ienumpstoretypes-clone.md) | <span data-ttu-id="b26da-118">Crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="b26da-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="b26da-119">**Next**</span><span class="sxs-lookup"><span data-stu-id="b26da-119">**Next**</span></span>](ienumpstoretypes-next.md)   | <span data-ttu-id="b26da-120">Obtiene el siguiente tipo de proveedor especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="b26da-120">Gets the next specified provider type in the enumeration sequence.</span></span><br/>                      |
| [<span data-ttu-id="b26da-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b26da-121">**Reset**</span></span>](ienumpstoretypes-reset.md) | <span data-ttu-id="b26da-122">Restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="b26da-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="b26da-123">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="b26da-123">**Skip**</span></span>](ienumpstoretypes-skip.md)   | <span data-ttu-id="b26da-124">Omite el tipo de proveedor especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="b26da-124">Skips the specified provider type in the enumeration sequence.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="b26da-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b26da-125">Remarks</span></span>

<span data-ttu-id="b26da-126">El objeto enumerador debe liberarse cuando ya no se esté utilizando.</span><span class="sxs-lookup"><span data-stu-id="b26da-126">The enumerator object must be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b26da-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b26da-127">Requirements</span></span>



| <span data-ttu-id="b26da-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b26da-128">Requirement</span></span> | <span data-ttu-id="b26da-129">Value</span><span class="sxs-lookup"><span data-stu-id="b26da-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b26da-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b26da-130">Header</span></span><br/> | <dl> <span data-ttu-id="b26da-131"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="b26da-131"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="b26da-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b26da-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="b26da-133"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b26da-133"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
