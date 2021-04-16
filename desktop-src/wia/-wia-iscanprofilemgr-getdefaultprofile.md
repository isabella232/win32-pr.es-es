---
description: Obtiene el perfil de detección predeterminado.
ms.assetid: 0e5ca06a-78ca-4d24-8dda-26babc3124b5
title: 'IScanProfileMgr:: GetDefaultProfile (método) (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetDefaultProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e058094fc29510d6e073abc0b05374403a2b5cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705782"
---
# <a name="iscanprofilemgrgetdefaultprofile-method"></a><span data-ttu-id="a384f-103">IScanProfileMgr:: GetDefaultProfile (método)</span><span class="sxs-lookup"><span data-stu-id="a384f-103">IScanProfileMgr::GetDefaultProfile method</span></span>

<span data-ttu-id="a384f-104">Obtiene el perfil de detección predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a384f-104">Gets the default scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="a384f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a384f-105">Syntax</span></span>


```C++
HRESULT GetDefaultProfile(
  [in]  BSTR         bstrDeviceID,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="a384f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a384f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a384f-107">*bstrDeviceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a384f-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a384f-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a384f-108">Type: **BSTR**</span></span>

<span data-ttu-id="a384f-109">IDENTIFICADOR del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a384f-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="a384f-110">*ppScanProfile* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a384f-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a384f-111">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a384f-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="a384f-112">Dirección de un puntero al perfil predeterminado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a384f-112">The address of a pointer to the device's default profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a384f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a384f-113">Return value</span></span>

<span data-ttu-id="a384f-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a384f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a384f-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a384f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a384f-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a384f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a384f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a384f-117">Remarks</span></span>

<span data-ttu-id="a384f-118">El perfil predeterminado tiene un `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="a384f-118">The default profile has a `<Default>` element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a384f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a384f-119">Requirements</span></span>



| <span data-ttu-id="a384f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a384f-120">Requirement</span></span> | <span data-ttu-id="a384f-121">Value</span><span class="sxs-lookup"><span data-stu-id="a384f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a384f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a384f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a384f-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a384f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a384f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a384f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a384f-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a384f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a384f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a384f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a384f-127"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="a384f-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="a384f-128">IDL</span><span class="sxs-lookup"><span data-stu-id="a384f-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a384f-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a384f-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a384f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a384f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a384f-131">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="a384f-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="a384f-132">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="a384f-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




