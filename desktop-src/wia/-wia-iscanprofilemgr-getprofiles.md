---
description: Obtiene todos los perfiles de digitalización disponibles para el usuario en el sistema en el que se ejecuta la aplicación.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'IScanProfileMgr:: GetProfiles (método) (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813883"
---
# <a name="iscanprofilemgrgetprofiles-method"></a><span data-ttu-id="940b4-103">IScanProfileMgr:: GetProfiles (método)</span><span class="sxs-lookup"><span data-stu-id="940b4-103">IScanProfileMgr::GetProfiles method</span></span>

<span data-ttu-id="940b4-104">Obtiene todos los perfiles de digitalización disponibles para el usuario en el sistema en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="940b4-104">Gets all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="940b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="940b4-105">Syntax</span></span>


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="940b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="940b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="940b4-107">*pulNumProfiles* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="940b4-107">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="940b4-108">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="940b4-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="940b4-109">Cuando se pasa, puntero al número máximo de perfiles que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="940b4-109">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="940b4-110">Cuando se devuelve, un puntero al número de perfiles devueltos.</span><span class="sxs-lookup"><span data-stu-id="940b4-110">When returned, a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="940b4-111">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="940b4-111">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="940b4-112">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="940b4-112">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="940b4-113">Dirección de una matriz de punteros a perfiles.</span><span class="sxs-lookup"><span data-stu-id="940b4-113">The address of an array of pointers to profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="940b4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="940b4-114">Return value</span></span>

<span data-ttu-id="940b4-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="940b4-115">Type: **HRESULT**</span></span>

<span data-ttu-id="940b4-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="940b4-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="940b4-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="940b4-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="940b4-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="940b4-118">Remarks</span></span>

<span data-ttu-id="940b4-119">Si el número total de perfiles disponibles para el usuario es menor que el valor pasado a *pulNumProfiles*, *pulNumProfiles* devuelve ese total.</span><span class="sxs-lookup"><span data-stu-id="940b4-119">If the total number of profiles available for the user is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="940b4-120">De lo contrario, devuelve el mismo valor que se le ha pasado.</span><span class="sxs-lookup"><span data-stu-id="940b4-120">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="940b4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="940b4-121">Requirements</span></span>



| <span data-ttu-id="940b4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="940b4-122">Requirement</span></span> | <span data-ttu-id="940b4-123">Value</span><span class="sxs-lookup"><span data-stu-id="940b4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="940b4-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="940b4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="940b4-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="940b4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="940b4-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="940b4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="940b4-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="940b4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="940b4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="940b4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="940b4-129"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="940b4-129"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="940b4-130">IDL</span><span class="sxs-lookup"><span data-stu-id="940b4-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="940b4-131"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="940b4-131"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="940b4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="940b4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940b4-133">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="940b4-133">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="940b4-134">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="940b4-134">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




