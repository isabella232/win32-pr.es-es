---
description: Crea un perfil de digitalización vacío y lo asocia a un escáner u otro elemento 2,0 de adquisición de imágenes de Windows (WIA).
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'IScanProfileMgr:: CreateProfile (método) (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497723"
---
# <a name="iscanprofilemgrcreateprofile-method"></a><span data-ttu-id="e7b7d-103">IScanProfileMgr:: CreateProfile (método)</span><span class="sxs-lookup"><span data-stu-id="e7b7d-103">IScanProfileMgr::CreateProfile method</span></span>

<span data-ttu-id="e7b7d-104">Crea un perfil de digitalización vacío y lo asocia a un escáner u otro elemento 2,0 de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="e7b7d-104">Creates an empty scan profile and associates it with a scanner or other Windows Image Acquisition (WIA) 2.0 item.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b7d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7b7d-105">Syntax</span></span>


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="e7b7d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7b7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b7d-107">*bstrDeviceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7b7d-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b7d-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7b7d-108">Type: **BSTR**</span></span>

<span data-ttu-id="e7b7d-109">El identificador del dispositivo o el elemento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="e7b7d-109">The ID of the device or WIA 2.0 item.</span></span>

</dd> <dt>

<span data-ttu-id="e7b7d-110">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7b7d-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b7d-111">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7b7d-111">Type: **BSTR**</span></span>

<span data-ttu-id="e7b7d-112">Nombre descriptivo del nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="e7b7d-112">The friendly name of the new profile.</span></span>

</dd> <dt>

<span data-ttu-id="e7b7d-113">*guidCategory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7b7d-113">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b7d-114">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="e7b7d-114">Type: **GUID**</span></span>

<span data-ttu-id="e7b7d-115">El GUID de la categoría del dispositivo o el elemento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="e7b7d-115">The GUID of the category of the device or WIA 2.0 item.</span></span> <span data-ttu-id="e7b7d-116">Debe ser una de las constantes de \_ categoría de elemento IPA de WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e7b7d-116">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> <dt>

<span data-ttu-id="e7b7d-117">*ppScanProfile* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e7b7d-117">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b7d-118">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e7b7d-118">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="e7b7d-119">Dirección de un puntero al nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="e7b7d-119">The address of a pointer to the new profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b7d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7b7d-120">Return value</span></span>

<span data-ttu-id="e7b7d-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7b7d-121">Type: **HRESULT**</span></span>

<span data-ttu-id="e7b7d-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e7b7d-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7b7d-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7b7d-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b7d-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7b7d-124">Remarks</span></span>

<span data-ttu-id="e7b7d-125">**IScanProfileMgr:: CreateProfile** asocia el dispositivo especificado con el nuevo perfil de digitalización.</span><span class="sxs-lookup"><span data-stu-id="e7b7d-125">**IScanProfileMgr::CreateProfile** associates the specified device with the new scan profile.</span></span>

<span data-ttu-id="e7b7d-126">**IScanProfileMgr:: CreateProfile** genera automáticamente un GUID para el nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="e7b7d-126">**IScanProfileMgr::CreateProfile** automatically generates a GUID for the new profile.</span></span> <span data-ttu-id="e7b7d-127">Obtiene el GUID con [**GetGUID**](-wia-iscanprofile-getguid.md).</span><span class="sxs-lookup"><span data-stu-id="e7b7d-127">Get the GUID with [**GetGUID**](-wia-iscanprofile-getguid.md).</span></span>

<span data-ttu-id="e7b7d-128">Use el método [**IScanProfileMgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) cuando más de un objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) pueda estar creando o eliminando perfiles al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e7b7d-128">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b7d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7b7d-129">Requirements</span></span>



| <span data-ttu-id="e7b7d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b7d-130">Requirement</span></span> | <span data-ttu-id="e7b7d-131">Value</span><span class="sxs-lookup"><span data-stu-id="e7b7d-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b7d-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7b7d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b7d-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e7b7d-133">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e7b7d-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7b7d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b7d-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7b7d-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7b7d-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7b7d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7b7d-137"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b7d-137"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="e7b7d-138">IDL</span><span class="sxs-lookup"><span data-stu-id="e7b7d-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7b7d-139"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7b7d-139"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b7d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7b7d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b7d-141">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="e7b7d-141">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="e7b7d-142">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="e7b7d-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




