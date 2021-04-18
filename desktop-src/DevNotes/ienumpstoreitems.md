---
description: Proporciona los métodos de enumeración estándar de COM para la interfaz IPStore.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Interfaz IEnumPStoreItems (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660371"
---
# <a name="ienumpstoreitems-interface"></a><span data-ttu-id="4a2e5-103">Interfaz IEnumPStoreItems</span><span class="sxs-lookup"><span data-stu-id="4a2e5-103">IEnumPStoreItems interface</span></span>

<span data-ttu-id="4a2e5-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a2e5-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4a2e5-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4a2e5-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4a2e5-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="4a2e5-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4a2e5-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="4a2e5-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4a2e5-108">Proporciona los métodos de enumeración estándar de COM para la interfaz [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="4a2e5-108">Provides the COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="4a2e5-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4a2e5-109">Members</span></span>

<span data-ttu-id="4a2e5-110">La interfaz **IEnumPStoreItems** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4a2e5-110">The **IEnumPStoreItems** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4a2e5-111">**IEnumPStoreItems** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4a2e5-111">**IEnumPStoreItems** also has these types of members:</span></span>

-   [<span data-ttu-id="4a2e5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a2e5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4a2e5-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a2e5-113">Methods</span></span>

<span data-ttu-id="4a2e5-114">La interfaz **IEnumPStoreItems** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4a2e5-114">The **IEnumPStoreItems** interface has these methods.</span></span>



| <span data-ttu-id="4a2e5-115">Método</span><span class="sxs-lookup"><span data-stu-id="4a2e5-115">Method</span></span>                                  | <span data-ttu-id="4a2e5-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a2e5-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a2e5-117">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="4a2e5-117">**Clone**</span></span>](ienumpstoreitems-clone.md) | <span data-ttu-id="4a2e5-118">Crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="4a2e5-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="4a2e5-119">**Next**</span><span class="sxs-lookup"><span data-stu-id="4a2e5-119">**Next**</span></span>](ienumpstoreitems-next.md)   | <span data-ttu-id="4a2e5-120">Obtiene el siguiente elemento de datos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="4a2e5-120">Gets the next specified data item in the enumeration sequence.</span></span><br/>                          |
| [<span data-ttu-id="4a2e5-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="4a2e5-121">**Reset**</span></span>](ienumpstoreitems-reset.md) | <span data-ttu-id="4a2e5-122">Se restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="4a2e5-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="4a2e5-123">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="4a2e5-123">**Skip**</span></span>](ienumpstoreitems-skip.md)   | <span data-ttu-id="4a2e5-124">Omite el elemento de datos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="4a2e5-124">Skips the specified data item in the enumeration sequence.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="4a2e5-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a2e5-125">Remarks</span></span>

<span data-ttu-id="4a2e5-126">Es necesario liberar cada elemento después de enumerarlo.</span><span class="sxs-lookup"><span data-stu-id="4a2e5-126">It is necessary to free each item after enumerating it.</span></span> <span data-ttu-id="4a2e5-127">También se debe liberar el objeto de enumerador cuando ya no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4a2e5-127">The enumerator object must also be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a2e5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a2e5-128">Requirements</span></span>



| <span data-ttu-id="4a2e5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a2e5-129">Requirement</span></span> | <span data-ttu-id="4a2e5-130">Value</span><span class="sxs-lookup"><span data-stu-id="4a2e5-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2e5-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a2e5-131">Header</span></span><br/> | <dl> <span data-ttu-id="4a2e5-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e5-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="4a2e5-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a2e5-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="4a2e5-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e5-134"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
