---
description: Recupera un puntero de interfaz a un proveedor de almacenamiento.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Función PStoreCreateInstance (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649889"
---
# <a name="pstorecreateinstance-function"></a><span data-ttu-id="545a7-103">PStoreCreateInstance función)</span><span class="sxs-lookup"><span data-stu-id="545a7-103">PStoreCreateInstance function</span></span>

<span data-ttu-id="545a7-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="545a7-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="545a7-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="545a7-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="545a7-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="545a7-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="545a7-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="545a7-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="545a7-108">\[Esta función puede modificarse o no estar disponible en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="545a7-108">\[This function may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="545a7-109">Use las funciones **CryptProtectData** y **CryptUnprotectData** en lugar de esta función.\]</span><span class="sxs-lookup"><span data-stu-id="545a7-109">Use the **CryptProtectData** and **CryptUnprotectData** functions instead of this function.\]</span></span>

<span data-ttu-id="545a7-110">Recupera un puntero de interfaz a un proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="545a7-110">Retrieves an interface pointer to a storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="545a7-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="545a7-111">Syntax</span></span>


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="545a7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="545a7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="545a7-113">*ppProvider* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="545a7-113">*ppProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="545a7-114">Puntero al puntero de interfaz recuperado para el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="545a7-114">A pointer to the retrieved interface pointer for the storage provider.</span></span> <span data-ttu-id="545a7-115">Cuando termine de usar la interfaz, disminuya su recuento de referencias mediante una llamada a su método [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="545a7-115">When you finish using the interface, decrement its reference count by calling its [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="545a7-116">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="545a7-116">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="545a7-117">*pProviderID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="545a7-117">*pProviderID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="545a7-118">Puntero al **GUID** que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="545a7-118">A pointer to the **GUID** that identifies the storage provider.</span></span> <span data-ttu-id="545a7-119">Si este parámetro es **null**, se usa el proveedor de almacenamiento base.</span><span class="sxs-lookup"><span data-stu-id="545a7-119">If this parameter is **NULL**, then the base storage provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="545a7-120">*conservado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="545a7-120">*pReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="545a7-121">Sector debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="545a7-121">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="545a7-122">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="545a7-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="545a7-123">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="545a7-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="545a7-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="545a7-124">Return value</span></span>

<span data-ttu-id="545a7-125">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="545a7-125">The return value is an **HRESULT**.</span></span> <span data-ttu-id="545a7-126">Un valor de **S \_ correcto** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="545a7-126">A value of **S\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="545a7-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="545a7-127">Remarks</span></span>

<span data-ttu-id="545a7-128">Esta función no tiene biblioteca de importación asociada. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="545a7-128">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="545a7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="545a7-129">Requirements</span></span>



| <span data-ttu-id="545a7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="545a7-130">Requirement</span></span> | <span data-ttu-id="545a7-131">Value</span><span class="sxs-lookup"><span data-stu-id="545a7-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="545a7-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="545a7-132">Header</span></span><br/> | <dl> <span data-ttu-id="545a7-133"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="545a7-133"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="545a7-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="545a7-134">DLL</span></span><br/>    | <dl> <span data-ttu-id="545a7-135"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="545a7-135"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="545a7-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="545a7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="545a7-137">**CryptProtectData**</span><span class="sxs-lookup"><span data-stu-id="545a7-137">**CryptProtectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[<span data-ttu-id="545a7-138">**CryptUnprotectData**</span><span class="sxs-lookup"><span data-stu-id="545a7-138">**CryptUnprotectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
