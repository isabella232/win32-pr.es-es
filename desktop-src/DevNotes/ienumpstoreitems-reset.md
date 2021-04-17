---
description: Restablece al principio de la secuencia de enumeración especificada.
ms.assetid: add91f5d-3f84-4069-93c0-9380a3935b85
title: 'IEnumPStoreItems:: RESET (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d5b05c23ba40ab647b2c4b3bb552f92ee34e12c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661155"
---
# <a name="ienumpstoreitemsreset-method"></a><span data-ttu-id="8338e-103">IEnumPStoreItems:: RESET (método)</span><span class="sxs-lookup"><span data-stu-id="8338e-103">IEnumPStoreItems::Reset method</span></span>

<span data-ttu-id="8338e-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8338e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="8338e-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8338e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="8338e-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="8338e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="8338e-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="8338e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="8338e-108">Restablece al principio de la secuencia de enumeración especificada.</span><span class="sxs-lookup"><span data-stu-id="8338e-108">Resets to the beginning of the given enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="8338e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8338e-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="8338e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8338e-110">Parameters</span></span>

<span data-ttu-id="8338e-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8338e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8338e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8338e-112">Return value</span></span>

<span data-ttu-id="8338e-113">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8338e-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8338e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8338e-114">Requirements</span></span>



| <span data-ttu-id="8338e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8338e-115">Requirement</span></span> | <span data-ttu-id="8338e-116">Value</span><span class="sxs-lookup"><span data-stu-id="8338e-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8338e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8338e-117">Header</span></span><br/> | <dl> <span data-ttu-id="8338e-118"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="8338e-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="8338e-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8338e-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="8338e-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8338e-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8338e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8338e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8338e-122">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="8338e-122">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
