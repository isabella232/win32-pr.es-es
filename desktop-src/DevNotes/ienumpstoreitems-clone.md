---
description: Crea otro enumerador que contiene el mismo estado de enumeración que el actual.
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: 'IEnumPStoreItems:: Clone (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 919c0359f5c7f6d3ab547f53a105246c43e20fb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661156"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="759ae-103">IEnumPStoreItems:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="759ae-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="759ae-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="759ae-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="759ae-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="759ae-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="759ae-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="759ae-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="759ae-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="759ae-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="759ae-108">Crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="759ae-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="759ae-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="759ae-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="759ae-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="759ae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="759ae-111">*ppenum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="759ae-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="759ae-112">Un puntero a un puntero [**IEnumPStoreItems**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="759ae-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="759ae-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="759ae-113">Return value</span></span>

<span data-ttu-id="759ae-114">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="759ae-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="759ae-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="759ae-115">Requirements</span></span>



| <span data-ttu-id="759ae-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="759ae-116">Requirement</span></span> | <span data-ttu-id="759ae-117">Value</span><span class="sxs-lookup"><span data-stu-id="759ae-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="759ae-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="759ae-118">Header</span></span><br/> | <dl> <span data-ttu-id="759ae-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="759ae-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="759ae-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="759ae-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="759ae-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="759ae-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="759ae-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="759ae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="759ae-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="759ae-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
