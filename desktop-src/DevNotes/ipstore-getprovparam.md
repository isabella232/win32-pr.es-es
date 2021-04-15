---
description: Diseñado para establecer la información de parámetros especificada.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'IPStore:: GetProvParam (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649521"
---
# <a name="ipstoregetprovparam-method"></a><span data-ttu-id="0810b-103">IPStore:: GetProvParam (método)</span><span class="sxs-lookup"><span data-stu-id="0810b-103">IPStore::GetProvParam method</span></span>

<span data-ttu-id="0810b-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0810b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0810b-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0810b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0810b-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="0810b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0810b-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="0810b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0810b-108">\[Este método no se implementa.\]</span><span class="sxs-lookup"><span data-stu-id="0810b-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="0810b-109">Diseñado para establecer la información de parámetros especificada.</span><span class="sxs-lookup"><span data-stu-id="0810b-109">Intended to set the specified parameter information.</span></span> <span data-ttu-id="0810b-110">Sin embargo, tenga en cuenta que no se implementa y que siempre producirá un error.</span><span class="sxs-lookup"><span data-stu-id="0810b-110">Note, however, that it is not implemented and will always fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="0810b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0810b-111">Syntax</span></span>


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0810b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0810b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0810b-113">*dwParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0810b-113">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0810b-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0810b-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0810b-115">*pcbData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0810b-115">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0810b-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0810b-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0810b-117">*ppbData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0810b-117">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0810b-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0810b-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0810b-119">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0810b-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0810b-120">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0810b-120">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0810b-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0810b-121">Return value</span></span>

<span data-ttu-id="0810b-122">Siempre se producirá un error en las llamadas a este método.</span><span class="sxs-lookup"><span data-stu-id="0810b-122">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="0810b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0810b-123">Requirements</span></span>



| <span data-ttu-id="0810b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0810b-124">Requirement</span></span> | <span data-ttu-id="0810b-125">Value</span><span class="sxs-lookup"><span data-stu-id="0810b-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0810b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0810b-126">Header</span></span><br/> | <dl> <span data-ttu-id="0810b-127"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="0810b-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0810b-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0810b-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="0810b-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0810b-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0810b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0810b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0810b-131">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="0810b-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
