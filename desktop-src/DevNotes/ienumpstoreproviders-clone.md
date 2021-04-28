---
description: 'Método IEnumPStoreProviders::Clone: crea otro enumerador que contiene el mismo estado de enumeración que el actual.'
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: Método IEnumPStoreProviders::Clone (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2eb5f5788c903c854d9cf1551d6cf5a1bd2b51f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096803"
---
# <a name="ienumpstoreprovidersclone-method"></a><span data-ttu-id="7f90b-103">IEnumPStoreProviders::Clone (Método)</span><span class="sxs-lookup"><span data-stu-id="7f90b-103">IEnumPStoreProviders::Clone method</span></span>

<span data-ttu-id="7f90b-104">\[El almacenamiento protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7f90b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="7f90b-105">Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7f90b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="7f90b-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="7f90b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="7f90b-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="7f90b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="7f90b-108">Crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="7f90b-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f90b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f90b-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="7f90b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f90b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f90b-111">*laum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7f90b-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f90b-112">Puntero a un [**puntero IEnumPStoreProviders.**](ienumpstoreproviders.md)</span><span class="sxs-lookup"><span data-stu-id="7f90b-112">A pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f90b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f90b-113">Return value</span></span>

<span data-ttu-id="7f90b-114">El valor devuelto es **un valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="7f90b-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f90b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f90b-115">Requirements</span></span>



| <span data-ttu-id="7f90b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f90b-116">Requirement</span></span> | <span data-ttu-id="7f90b-117">Value</span><span class="sxs-lookup"><span data-stu-id="7f90b-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f90b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f90b-118">Header</span></span><br/> | <dl> <span data-ttu-id="7f90b-119"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="7f90b-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="7f90b-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7f90b-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="7f90b-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f90b-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f90b-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7f90b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f90b-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="7f90b-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
