---
description: Elimina el perfil de digitalización especificado.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: IScanProfileMgr::D método eleteProfile (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002036"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a><span data-ttu-id="935b5-103">IScanProfileMgr::D método eleteProfile</span><span class="sxs-lookup"><span data-stu-id="935b5-103">IScanProfileMgr::DeleteProfile method</span></span>

<span data-ttu-id="935b5-104">Elimina el perfil de digitalización especificado.</span><span class="sxs-lookup"><span data-stu-id="935b5-104">Deletes the specified scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="935b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="935b5-105">Syntax</span></span>


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="935b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="935b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="935b5-107">*pScanProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="935b5-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="935b5-108">Tipo: \**[**IScanProfile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="935b5-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="935b5-109">Puntero al perfil.</span><span class="sxs-lookup"><span data-stu-id="935b5-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="935b5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="935b5-110">Return value</span></span>

<span data-ttu-id="935b5-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="935b5-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="935b5-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="935b5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="935b5-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="935b5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="935b5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="935b5-114">Remarks</span></span>

<span data-ttu-id="935b5-115">**IScanProfileMgr::D eleteprofile** elimina el perfil del disco y destruye el objeto de perfil en la memoria.</span><span class="sxs-lookup"><span data-stu-id="935b5-115">**IScanProfileMgr::DeleteProfile** deletes the profile from disk and destroys the profile object in memory.</span></span>

<span data-ttu-id="935b5-116">Use el método [**IScanProfileMgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) cuando más de un objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) pueda estar creando o eliminando perfiles al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="935b5-116">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="935b5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="935b5-117">Requirements</span></span>



| <span data-ttu-id="935b5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="935b5-118">Requirement</span></span> | <span data-ttu-id="935b5-119">Value</span><span class="sxs-lookup"><span data-stu-id="935b5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="935b5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="935b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="935b5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="935b5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="935b5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="935b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="935b5-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="935b5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="935b5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="935b5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="935b5-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="935b5-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="935b5-126">IDL</span><span class="sxs-lookup"><span data-stu-id="935b5-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="935b5-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="935b5-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="935b5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="935b5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935b5-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="935b5-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="935b5-130">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="935b5-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




