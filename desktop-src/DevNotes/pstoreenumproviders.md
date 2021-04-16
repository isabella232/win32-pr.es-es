---
description: Obtiene un objeto de enumerador que se puede utilizar a su vez para enumerar los proveedores de almacenamiento protegidos que están instalados actualmente en el sistema.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Función PStoreEnumProviders (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650000"
---
# <a name="pstoreenumproviders-function"></a><span data-ttu-id="fb9be-103">PStoreEnumProviders función)</span><span class="sxs-lookup"><span data-stu-id="fb9be-103">PStoreEnumProviders function</span></span>

<span data-ttu-id="fb9be-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fb9be-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="fb9be-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fb9be-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="fb9be-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="fb9be-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="fb9be-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="fb9be-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="fb9be-108">Obtiene un objeto de enumerador que se puede utilizar a su vez para enumerar los proveedores de almacenamiento protegidos que están instalados actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="fb9be-108">Gets an enumerator object that can be used in turn to enumerate the protected storage providers that are currently installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb9be-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb9be-109">Syntax</span></span>


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="fb9be-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb9be-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb9be-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="fb9be-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="fb9be-112">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fb9be-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fb9be-113">*ppenum*</span><span class="sxs-lookup"><span data-stu-id="fb9be-113">*ppenum*</span></span> 
</dt> <dd>

<span data-ttu-id="fb9be-114">Un puntero a un puntero a una interfaz [**IEnumPStoreProviders**](ienumpstoreproviders.md) que se puede usar para enumerar los proveedores instalados.</span><span class="sxs-lookup"><span data-stu-id="fb9be-114">A pointer to a pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) interface that can be used to enumerate installed providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb9be-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb9be-115">Return value</span></span>

<span data-ttu-id="fb9be-116">Esta función devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fb9be-116">This function returns an **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb9be-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb9be-117">Remarks</span></span>

<span data-ttu-id="fb9be-118">El componente de almacenamiento protegido tiene una arquitectura basada en proveedor.</span><span class="sxs-lookup"><span data-stu-id="fb9be-118">The protected storage component has a provider-based architecture.</span></span> <span data-ttu-id="fb9be-119">Las aplicaciones que hacen uso de almacenamiento protegido pueden especificar los proveedores instalados que se van a usar al almacenar y recuperar sus datos.</span><span class="sxs-lookup"><span data-stu-id="fb9be-119">Applications that make use of protected storage can specify which of the installed providers to use when storing and retrieving their data.</span></span>

<span data-ttu-id="fb9be-120">La función **PStoreEnumProviders** se usa para enumerar los proveedores de almacenamiento protegido instalados.</span><span class="sxs-lookup"><span data-stu-id="fb9be-120">The **PStoreEnumProviders** function is used to enumerate the installed protected storage providers.</span></span> <span data-ttu-id="fb9be-121">Cada proveedor se identifica mediante un identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="fb9be-121">Each provider is identified by a globally unique identifier (GUID).</span></span>

<span data-ttu-id="fb9be-122">Hasta este momento, solo se ha escrito un proveedor de almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="fb9be-122">Up to this time, only one protected storage provider has ever been written.</span></span> <span data-ttu-id="fb9be-123">Dado que el servicio de almacenamiento protegido está en desuso actualmente, es muy poco probable que se produzcan todos los proveedores adicionales.</span><span class="sxs-lookup"><span data-stu-id="fb9be-123">Given that the protected storage service is currently deprecated, it is very unlikely that any additional providers will ever be produced.</span></span> <span data-ttu-id="fb9be-124">Como resultado, esta función no se debe usar para ningún propósito.</span><span class="sxs-lookup"><span data-stu-id="fb9be-124">As a result, this function should not be used for any purpose.</span></span>

<span data-ttu-id="fb9be-125">Esta función no tiene biblioteca de importación asociada. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="fb9be-125">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb9be-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb9be-126">Requirements</span></span>



| <span data-ttu-id="fb9be-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb9be-127">Requirement</span></span> | <span data-ttu-id="fb9be-128">Value</span><span class="sxs-lookup"><span data-stu-id="fb9be-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9be-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb9be-129">Header</span></span><br/> | <dl> <span data-ttu-id="fb9be-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb9be-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="fb9be-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb9be-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="fb9be-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb9be-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb9be-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb9be-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9be-134">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="fb9be-134">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
