---
description: 'Método IEnumPStoreProviders::Skip: omite el siguiente número especificado de elementos en la secuencia de enumeración.'
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: Método IEnumPStoreProviders::Skip (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2f74c44de172d9235d9768b8f484405b5e8fb7fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096753"
---
# <a name="ienumpstoreprovidersskip-method"></a><span data-ttu-id="44295-103">IEnumPStoreProviders::Skip (Método)</span><span class="sxs-lookup"><span data-stu-id="44295-103">IEnumPStoreProviders::Skip method</span></span>

<span data-ttu-id="44295-104">\[El almacenamiento protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="44295-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="44295-105">Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="44295-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="44295-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="44295-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="44295-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="44295-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="44295-108">Omite el siguiente número especificado de elementos en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="44295-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="44295-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44295-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="44295-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44295-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44295-111">*celta* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="44295-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44295-112">Número de tipos de proveedor que se omitirán.</span><span class="sxs-lookup"><span data-stu-id="44295-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44295-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44295-113">Return value</span></span>

<span data-ttu-id="44295-114">El valor devuelto es **un valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="44295-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="44295-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44295-115">Requirements</span></span>



| <span data-ttu-id="44295-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44295-116">Requirement</span></span> | <span data-ttu-id="44295-117">Value</span><span class="sxs-lookup"><span data-stu-id="44295-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44295-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44295-118">Header</span></span><br/> | <dl> <span data-ttu-id="44295-119"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="44295-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="44295-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44295-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="44295-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44295-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44295-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="44295-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44295-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="44295-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
