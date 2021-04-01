---
description: Obtiene el número de perfiles de examen para el dispositivo.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'IScanProfileMgr:: GetNumProfilesforDeviceID (método) (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275636"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a><span data-ttu-id="dad5f-103">IScanProfileMgr:: GetNumProfilesforDeviceID (método)</span><span class="sxs-lookup"><span data-stu-id="dad5f-103">IScanProfileMgr::GetNumProfilesforDeviceID method</span></span>

<span data-ttu-id="dad5f-104">Obtiene el número de perfiles de examen para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dad5f-104">Gets the number of scan profiles for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="dad5f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dad5f-105">Syntax</span></span>


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="dad5f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dad5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dad5f-107">*bstrDeviceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dad5f-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad5f-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dad5f-108">Type: **BSTR**</span></span>

<span data-ttu-id="dad5f-109">IDENTIFICADOR del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dad5f-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="dad5f-110">*pulNumProfiles* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dad5f-110">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dad5f-111">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="dad5f-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="dad5f-112">Un puntero al número de perfiles disponibles para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dad5f-112">A pointer to the number of profiles available for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dad5f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dad5f-113">Return value</span></span>

<span data-ttu-id="dad5f-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="dad5f-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="dad5f-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="dad5f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dad5f-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dad5f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad5f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dad5f-117">Requirements</span></span>



| <span data-ttu-id="dad5f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dad5f-118">Requirement</span></span> | <span data-ttu-id="dad5f-119">Value</span><span class="sxs-lookup"><span data-stu-id="dad5f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dad5f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dad5f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dad5f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dad5f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="dad5f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dad5f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dad5f-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dad5f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dad5f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dad5f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dad5f-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="dad5f-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="dad5f-126">IDL</span><span class="sxs-lookup"><span data-stu-id="dad5f-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dad5f-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dad5f-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dad5f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="dad5f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad5f-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="dad5f-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="dad5f-130">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="dad5f-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




