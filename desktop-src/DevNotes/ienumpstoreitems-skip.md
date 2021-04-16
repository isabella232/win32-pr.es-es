---
description: Omite el siguiente número de elementos especificado en la secuencia de enumeración especificada.
ms.assetid: 1459c18a-ccff-451f-8904-32858cc72b78
title: 'IEnumPStoreItems:: Skip (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 912dea836ec5ac04ddaf54de9f7f7b609e4e23ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650133"
---
# <a name="ienumpstoreitemsskip-method"></a><span data-ttu-id="081b1-103">IEnumPStoreItems:: Skip (método)</span><span class="sxs-lookup"><span data-stu-id="081b1-103">IEnumPStoreItems::Skip method</span></span>

<span data-ttu-id="081b1-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="081b1-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="081b1-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="081b1-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="081b1-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="081b1-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="081b1-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="081b1-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="081b1-108">Omite el siguiente número de elementos especificado en la secuencia de enumeración especificada.</span><span class="sxs-lookup"><span data-stu-id="081b1-108">Skips over the next specified number of items in the given enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="081b1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="081b1-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="081b1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="081b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="081b1-111">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="081b1-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="081b1-112">Número de elementos de datos que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="081b1-112">The number of data items to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="081b1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="081b1-113">Return value</span></span>

<span data-ttu-id="081b1-114">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="081b1-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="081b1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="081b1-115">Requirements</span></span>



| <span data-ttu-id="081b1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="081b1-116">Requirement</span></span> | <span data-ttu-id="081b1-117">Value</span><span class="sxs-lookup"><span data-stu-id="081b1-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="081b1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="081b1-118">Header</span></span><br/> | <dl> <span data-ttu-id="081b1-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="081b1-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="081b1-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="081b1-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="081b1-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="081b1-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="081b1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="081b1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="081b1-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="081b1-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
