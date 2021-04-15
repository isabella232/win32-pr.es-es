---
description: Establece la información de parámetros especificada.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'IPStore:: SetProvParam (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: edbbb7bd2f5d889568623390d805659e1cf840f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649520"
---
# <a name="ipstoresetprovparam-method"></a><span data-ttu-id="6c4c8-103">IPStore:: SetProvParam (método)</span><span class="sxs-lookup"><span data-stu-id="6c4c8-103">IPStore::SetProvParam method</span></span>

<span data-ttu-id="6c4c8-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6c4c8-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6c4c8-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6c4c8-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="6c4c8-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6c4c8-108">Establece la información de parámetros especificada.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-108">Sets the specified parameter information.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c4c8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c4c8-109">Syntax</span></span>


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6c4c8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c4c8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c4c8-111">*dwParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c4c8-111">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4c8-112">Contiene la caché de contraseñas de **\_ \_ vaciado \_ \_ de PST PP** para vaciar la memoria caché de contraseñas de usuario.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-112">Contains **PST\_PP\_FLUSH\_PW\_CACHE** to flush the user password cache.</span></span>

</dd> <dt>

<span data-ttu-id="6c4c8-113">*cbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c4c8-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4c8-114">Longitud de la contraseña en el búfer.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-114">The length of the password in the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6c4c8-115">*pbData*</span><span class="sxs-lookup"><span data-stu-id="6c4c8-115">*pbData*</span></span> 
</dt> <dd>

<span data-ttu-id="6c4c8-116">Un puntero a un búfer que contiene la contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-116">A pointer to a buffer that contains the user's password.</span></span> <span data-ttu-id="6c4c8-117">Debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-117">This must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6c4c8-118">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6c4c8-118">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="6c4c8-119">Reserved: debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-119">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c4c8-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c4c8-120">Return value</span></span>

<span data-ttu-id="6c4c8-121">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6c4c8-121">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="6c4c8-122">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-122">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c4c8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c4c8-123">Requirements</span></span>



| <span data-ttu-id="6c4c8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c4c8-124">Requirement</span></span> | <span data-ttu-id="6c4c8-125">Value</span><span class="sxs-lookup"><span data-stu-id="6c4c8-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c4c8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c4c8-126">Header</span></span><br/> | <dl> <span data-ttu-id="6c4c8-127"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c4c8-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6c4c8-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c4c8-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="6c4c8-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c4c8-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c4c8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c4c8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4c8-131">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="6c4c8-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
