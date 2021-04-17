---
description: Devuelve información sobre el proveedor de almacenamiento.
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: 'IPStore:: GetInfo (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7747c3acf15a60f5556a8855ef4825715ef5050b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670358"
---
# <a name="ipstoregetinfo-method"></a><span data-ttu-id="afc63-103">IPStore:: GetInfo (método)</span><span class="sxs-lookup"><span data-stu-id="afc63-103">IPStore::GetInfo method</span></span>

<span data-ttu-id="afc63-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="afc63-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="afc63-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="afc63-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="afc63-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="afc63-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="afc63-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="afc63-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="afc63-108">Devuelve información sobre el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="afc63-108">Returns information on the storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc63-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afc63-109">Syntax</span></span>


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="afc63-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afc63-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc63-111">*ppProperties* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="afc63-111">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afc63-112">Puntero a una estructura de **PPST \_ providerinfo devuelto por** que contiene información sobre el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="afc63-112">A pointer to a **PPST\_PROVIDERINFO** structure that contains information about the storage provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc63-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afc63-113">Return value</span></span>

<span data-ttu-id="afc63-114">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="afc63-114">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="afc63-115">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="afc63-115">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc63-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afc63-116">Requirements</span></span>



| <span data-ttu-id="afc63-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="afc63-117">Requirement</span></span> | <span data-ttu-id="afc63-118">Value</span><span class="sxs-lookup"><span data-stu-id="afc63-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afc63-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afc63-119">Header</span></span><br/> | <dl> <span data-ttu-id="afc63-120"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc63-120"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="afc63-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="afc63-121">DLL</span></span><br/>    | <dl> <span data-ttu-id="afc63-122"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afc63-122"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afc63-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="afc63-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc63-124">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="afc63-124">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
