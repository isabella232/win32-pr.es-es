---
description: Se restablece al principio de la secuencia de enumeración.
ms.assetid: 35f14aa5-92cb-4ad8-b80c-2550dedb7a7f
title: 'IEnumPStoreTypes:: RESET (método) (pstore. h)'
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
ms.openlocfilehash: 60aeb1f68bcbf18e903472fa736b5714076dfbfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649522"
---
# <a name="ienumpstoretypesreset-method"></a><span data-ttu-id="8c130-103">IEnumPStoreTypes:: RESET (método)</span><span class="sxs-lookup"><span data-stu-id="8c130-103">IEnumPStoreTypes::Reset method</span></span>

<span data-ttu-id="8c130-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8c130-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="8c130-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8c130-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="8c130-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="8c130-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="8c130-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="8c130-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="8c130-108">Se restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="8c130-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c130-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c130-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="8c130-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c130-110">Parameters</span></span>

<span data-ttu-id="8c130-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c130-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c130-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c130-112">Return value</span></span>

<span data-ttu-id="8c130-113">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c130-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c130-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c130-114">Requirements</span></span>



| <span data-ttu-id="8c130-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c130-115">Requirement</span></span> | <span data-ttu-id="8c130-116">Value</span><span class="sxs-lookup"><span data-stu-id="8c130-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c130-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c130-117">Header</span></span><br/> | <dl> <span data-ttu-id="8c130-118"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c130-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="8c130-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c130-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="8c130-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c130-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c130-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c130-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c130-122">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="8c130-122">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
