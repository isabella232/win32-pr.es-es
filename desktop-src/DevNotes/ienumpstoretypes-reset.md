---
description: 'Método IEnumPStoreTypes::Reset: restablece al principio de la secuencia de enumeración.'
ms.assetid: 35f14aa5-92cb-4ad8-b80c-2550dedb7a7f
title: Método IEnumPStoreTypes::Reset (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 55953a67d19ac94f792769974d860bae9b57f1ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089323"
---
# <a name="ienumpstoretypesreset-method"></a><span data-ttu-id="fa5a7-103">IEnumPStoreTypes::Reset (Método)</span><span class="sxs-lookup"><span data-stu-id="fa5a7-103">IEnumPStoreTypes::Reset method</span></span>

<span data-ttu-id="fa5a7-104">\[El almacenamiento protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="fa5a7-105">Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="fa5a7-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="fa5a7-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="fa5a7-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="fa5a7-108">Restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa5a7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa5a7-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="fa5a7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa5a7-110">Parameters</span></span>

<span data-ttu-id="fa5a7-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa5a7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa5a7-112">Return value</span></span>

<span data-ttu-id="fa5a7-113">El valor devuelto es **un valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="fa5a7-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa5a7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa5a7-114">Requirements</span></span>



| <span data-ttu-id="fa5a7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa5a7-115">Requirement</span></span> | <span data-ttu-id="fa5a7-116">Value</span><span class="sxs-lookup"><span data-stu-id="fa5a7-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5a7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa5a7-117">Header</span></span><br/> | <dl> <span data-ttu-id="fa5a7-118"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="fa5a7-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="fa5a7-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa5a7-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="fa5a7-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa5a7-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa5a7-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fa5a7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa5a7-122">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="fa5a7-122">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
