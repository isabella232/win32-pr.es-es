---
description: 'Método IEnumPStoreTypes::Skip: omite el siguiente número especificado de elementos en la secuencia de enumeración.'
ms.assetid: 4c02aac8-0496-4ad9-9863-2074b2c71902
title: Método IEnumPStoreTypes::Skip (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdc656af2a8f50d02d2f88545d189d9c9285a7f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096743"
---
# <a name="ienumpstoretypesskip-method"></a><span data-ttu-id="baae3-103">IEnumPStoreTypes::Skip (Método)</span><span class="sxs-lookup"><span data-stu-id="baae3-103">IEnumPStoreTypes::Skip method</span></span>

<span data-ttu-id="baae3-104">\[El almacenamiento protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="baae3-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="baae3-105">Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="baae3-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="baae3-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="baae3-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="baae3-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="baae3-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="baae3-108">Omite el siguiente número especificado de elementos en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="baae3-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="baae3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="baae3-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="baae3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baae3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baae3-111">*celta* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="baae3-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baae3-112">Número de tipos de proveedor que se omitirán.</span><span class="sxs-lookup"><span data-stu-id="baae3-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baae3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="baae3-113">Return value</span></span>

<span data-ttu-id="baae3-114">El valor devuelto es un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="baae3-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="baae3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baae3-115">Requirements</span></span>



| <span data-ttu-id="baae3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="baae3-116">Requirement</span></span> | <span data-ttu-id="baae3-117">Value</span><span class="sxs-lookup"><span data-stu-id="baae3-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="baae3-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="baae3-118">Header</span></span><br/> | <dl> <span data-ttu-id="baae3-119"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="baae3-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="baae3-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="baae3-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="baae3-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baae3-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baae3-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="baae3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baae3-123">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="baae3-123">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
