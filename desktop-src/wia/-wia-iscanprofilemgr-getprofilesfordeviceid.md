---
description: Obtiene todos los perfiles de análisis asociados a un dispositivo.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'IScanProfileMgr:: GetProfilesforDeviceID (método) (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 10a7d891a114fc36de3f91341febf1616a06ed22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705780"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a><span data-ttu-id="3b708-103">IScanProfileMgr:: GetProfilesforDeviceID (método)</span><span class="sxs-lookup"><span data-stu-id="3b708-103">IScanProfileMgr::GetProfilesforDeviceID method</span></span>

<span data-ttu-id="3b708-104">Obtiene todos los perfiles de análisis asociados a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b708-104">Gets all the scan profiles associated with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b708-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b708-105">Syntax</span></span>


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="3b708-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b708-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b708-107">*bstrDeviceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b708-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b708-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3b708-108">Type: **BSTR**</span></span>

<span data-ttu-id="3b708-109">IDENTIFICADOR del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b708-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="3b708-110">*pulNumProfiles* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3b708-110">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b708-111">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="3b708-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="3b708-112">Cuando se pasa, puntero al número máximo de perfiles que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="3b708-112">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="3b708-113">Cuando se devuelve, puntero al número de perfiles devueltos.</span><span class="sxs-lookup"><span data-stu-id="3b708-113">When returned, the a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="3b708-114">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3b708-114">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b708-115">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3b708-115">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="3b708-116">Dirección de un puntero a una matriz de perfiles.</span><span class="sxs-lookup"><span data-stu-id="3b708-116">The address of a pointer to an array of profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b708-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b708-117">Return value</span></span>

<span data-ttu-id="3b708-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3b708-118">Type: **HRESULT**</span></span>

<span data-ttu-id="3b708-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3b708-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b708-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b708-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b708-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b708-121">Remarks</span></span>

<span data-ttu-id="3b708-122">Si el número total de perfiles asociados con el dispositivo es menor que el valor pasado a *pulNumProfiles*, *pulNumProfiles* devuelve ese total.</span><span class="sxs-lookup"><span data-stu-id="3b708-122">If the total number of profiles associated with the device is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="3b708-123">De lo contrario, devuelve el mismo valor que se le ha pasado.</span><span class="sxs-lookup"><span data-stu-id="3b708-123">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b708-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b708-124">Requirements</span></span>



| <span data-ttu-id="3b708-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b708-125">Requirement</span></span> | <span data-ttu-id="3b708-126">Value</span><span class="sxs-lookup"><span data-stu-id="3b708-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b708-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b708-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3b708-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3b708-128">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3b708-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b708-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3b708-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b708-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b708-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b708-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b708-132"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b708-132"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="3b708-133">IDL</span><span class="sxs-lookup"><span data-stu-id="3b708-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b708-134"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b708-134"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b708-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b708-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b708-136">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="3b708-136">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="3b708-137">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="3b708-137">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




