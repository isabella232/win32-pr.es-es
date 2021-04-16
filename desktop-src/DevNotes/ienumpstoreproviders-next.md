---
description: Obtiene el siguiente número especificado de proveedores en la secuencia de enumeración.
ms.assetid: 9ef8d330-6f78-4063-825c-9cf5b4f283cf
title: 'IEnumPStoreProviders:: Next (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f468d29682c4e3767d4d8fe7d59e60976f103484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649650"
---
# <a name="ienumpstoreprovidersnext-method"></a><span data-ttu-id="d6a98-103">IEnumPStoreProviders:: Next (método)</span><span class="sxs-lookup"><span data-stu-id="d6a98-103">IEnumPStoreProviders::Next method</span></span>

<span data-ttu-id="d6a98-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6a98-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d6a98-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d6a98-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d6a98-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="d6a98-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d6a98-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="d6a98-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d6a98-108">Obtiene el siguiente número especificado de proveedores en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="d6a98-108">Gets the next specified number of providers in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a98-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6a98-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="d6a98-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6a98-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a98-111">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d6a98-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a98-112">El número de tipos de proveedor solicitados.</span><span class="sxs-lookup"><span data-stu-id="d6a98-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="d6a98-113">*rgelt* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d6a98-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a98-114">Puntero a una cadena en la que se va a devolver el nombre del tipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="d6a98-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="d6a98-115">*pceltFetched* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d6a98-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a98-116">Puntero al número de tipos de proveedor que se proporcionaron realmente.</span><span class="sxs-lookup"><span data-stu-id="d6a98-116">A pointer to the number of provider types that was actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a98-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6a98-117">Return value</span></span>

<span data-ttu-id="d6a98-118">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6a98-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6a98-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6a98-119">Requirements</span></span>



| <span data-ttu-id="d6a98-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6a98-120">Requirement</span></span> | <span data-ttu-id="d6a98-121">Value</span><span class="sxs-lookup"><span data-stu-id="d6a98-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a98-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6a98-122">Header</span></span><br/> | <dl> <span data-ttu-id="d6a98-123"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6a98-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d6a98-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6a98-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="d6a98-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6a98-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6a98-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6a98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a98-127">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="d6a98-127">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
