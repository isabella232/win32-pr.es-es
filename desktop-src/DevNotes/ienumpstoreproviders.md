---
description: Proporciona métodos de enumeración estándar de COM para la interfaz IPStore.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Interfaz IEnumPStoreProviders (pstore. h)
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
ms.openlocfilehash: e01bd28722fdb4d5a0ff7e3db4f715ddc1df2315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661179"
---
# <a name="ienumpstoreproviders-interface"></a><span data-ttu-id="797c8-103">Interfaz IEnumPStoreProviders</span><span class="sxs-lookup"><span data-stu-id="797c8-103">IEnumPStoreProviders interface</span></span>

<span data-ttu-id="797c8-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="797c8-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="797c8-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="797c8-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="797c8-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="797c8-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="797c8-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="797c8-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="797c8-108">Proporciona métodos de enumeración estándar de COM para la interfaz [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="797c8-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="797c8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="797c8-109">Members</span></span>

<span data-ttu-id="797c8-110">La interfaz **IEnumPStoreProviders** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="797c8-110">The **IEnumPStoreProviders** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="797c8-111">**IEnumPStoreProviders** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="797c8-111">**IEnumPStoreProviders** also has these types of members:</span></span>

-   [<span data-ttu-id="797c8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="797c8-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="797c8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="797c8-113">Methods</span></span>

<span data-ttu-id="797c8-114">La interfaz **IEnumPStoreProviders** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="797c8-114">The **IEnumPStoreProviders** interface has these methods.</span></span>



| <span data-ttu-id="797c8-115">Método</span><span class="sxs-lookup"><span data-stu-id="797c8-115">Method</span></span>                                      | <span data-ttu-id="797c8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="797c8-116">Description</span></span>                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="797c8-117">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="797c8-117">**Clone**</span></span>](ienumpstoreproviders-clone.md) | <span data-ttu-id="797c8-118">Crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="797c8-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="797c8-119">**Next**</span><span class="sxs-lookup"><span data-stu-id="797c8-119">**Next**</span></span>](ienumpstoreproviders-next.md)   | <span data-ttu-id="797c8-120">Obtiene el siguiente proveedor especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="797c8-120">Gets the next specified provider in the enumeration sequence.</span></span><br/>                           |
| [<span data-ttu-id="797c8-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="797c8-121">**Reset**</span></span>](ienumpstoreproviders-reset.md) | <span data-ttu-id="797c8-122">Se restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="797c8-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="797c8-123">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="797c8-123">**Skip**</span></span>](ienumpstoreproviders-skip.md)   | <span data-ttu-id="797c8-124">Omite el proveedor especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="797c8-124">Skips the specified provider in the enumeration sequence.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="797c8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="797c8-125">Requirements</span></span>



| <span data-ttu-id="797c8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="797c8-126">Requirement</span></span> | <span data-ttu-id="797c8-127">Value</span><span class="sxs-lookup"><span data-stu-id="797c8-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="797c8-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="797c8-128">Header</span></span><br/> | <dl> <span data-ttu-id="797c8-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="797c8-129"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="797c8-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="797c8-130">DLL</span></span><br/>    | <dl> <span data-ttu-id="797c8-131"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="797c8-131"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
