---
description: 'Interfaz IEnumPStoreProviders: proporciona métodos de enumeración com estándar para la interfaz IPStore.'
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Interfaz IEnumPStoreProviders (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089353"
---
# <a name="ienumpstoreproviders-interface"></a><span data-ttu-id="4a33b-103">IEnumPStoreProviders (interfaz)</span><span class="sxs-lookup"><span data-stu-id="4a33b-103">IEnumPStoreProviders interface</span></span>

<span data-ttu-id="4a33b-104">\[El almacenamiento protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a33b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4a33b-105">Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4a33b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4a33b-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="4a33b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4a33b-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="4a33b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4a33b-108">Proporciona métodos de enumeración com estándar para la [**interfaz IPStore.**](ipstore.md)</span><span class="sxs-lookup"><span data-stu-id="4a33b-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="4a33b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4a33b-109">Members</span></span>

<span data-ttu-id="4a33b-110">La **interfaz IEnumPStoreProviders** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="4a33b-110">The **IEnumPStoreProviders** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4a33b-111">**IEnumPStoreProviders también** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4a33b-111">**IEnumPStoreProviders** also has these types of members:</span></span>

-   [<span data-ttu-id="4a33b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a33b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4a33b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a33b-113">Methods</span></span>

<span data-ttu-id="4a33b-114">La **interfaz IEnumPStoreProviders** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4a33b-114">The **IEnumPStoreProviders** interface has these methods.</span></span>



| <span data-ttu-id="4a33b-115">Método</span><span class="sxs-lookup"><span data-stu-id="4a33b-115">Method</span></span>                                      | <span data-ttu-id="4a33b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a33b-116">Description</span></span>                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a33b-117">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="4a33b-117">**Clone**</span></span>](ienumpstoreproviders-clone.md) | <span data-ttu-id="4a33b-118">Crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="4a33b-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="4a33b-119">**Next**</span><span class="sxs-lookup"><span data-stu-id="4a33b-119">**Next**</span></span>](ienumpstoreproviders-next.md)   | <span data-ttu-id="4a33b-120">Obtiene el siguiente proveedor especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="4a33b-120">Gets the next specified provider in the enumeration sequence.</span></span><br/>                           |
| [<span data-ttu-id="4a33b-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="4a33b-121">**Reset**</span></span>](ienumpstoreproviders-reset.md) | <span data-ttu-id="4a33b-122">Restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="4a33b-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="4a33b-123">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="4a33b-123">**Skip**</span></span>](ienumpstoreproviders-skip.md)   | <span data-ttu-id="4a33b-124">Omite el proveedor especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="4a33b-124">Skips the specified provider in the enumeration sequence.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="4a33b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a33b-125">Requirements</span></span>



| <span data-ttu-id="4a33b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a33b-126">Requirement</span></span> | <span data-ttu-id="4a33b-127">Value</span><span class="sxs-lookup"><span data-stu-id="4a33b-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a33b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a33b-128">Header</span></span><br/> | <dl> <span data-ttu-id="4a33b-129"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="4a33b-129"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="4a33b-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a33b-130">DLL</span></span><br/>    | <dl> <span data-ttu-id="4a33b-131"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a33b-131"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
