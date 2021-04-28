---
description: 'Método IEnumPStoreProviders::Reset: restablece al principio de la secuencia de enumeración.'
ms.assetid: 9c5044b5-25a3-4d10-829b-ef4d8b5ac095
title: Método IEnumPStoreProviders::Reset (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3e37e131b6f67f94bb787051123be8eb430eb39e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096763"
---
# <a name="ienumpstoreprovidersreset-method"></a><span data-ttu-id="2dd21-103">IEnumPStoreProviders::Reset (Método)</span><span class="sxs-lookup"><span data-stu-id="2dd21-103">IEnumPStoreProviders::Reset method</span></span>

<span data-ttu-id="2dd21-104">\[El almacenamiento protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2dd21-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="2dd21-105">Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2dd21-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="2dd21-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="2dd21-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="2dd21-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="2dd21-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="2dd21-108">Restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="2dd21-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd21-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dd21-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="2dd21-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dd21-110">Parameters</span></span>

<span data-ttu-id="2dd21-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2dd21-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2dd21-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2dd21-112">Return value</span></span>

<span data-ttu-id="2dd21-113">El valor devuelto es **un valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="2dd21-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dd21-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dd21-114">Requirements</span></span>



| <span data-ttu-id="2dd21-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dd21-115">Requirement</span></span> | <span data-ttu-id="2dd21-116">Value</span><span class="sxs-lookup"><span data-stu-id="2dd21-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd21-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dd21-117">Header</span></span><br/> | <dl> <span data-ttu-id="2dd21-118"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="2dd21-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="2dd21-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2dd21-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="2dd21-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dd21-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dd21-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2dd21-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd21-122">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="2dd21-122">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
