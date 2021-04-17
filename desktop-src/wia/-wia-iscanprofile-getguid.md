---
description: Devuelve el GUID del perfil.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: 'IScanProfile:: GetGUID (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: e3c39815e1bc88830f64f632689028c4c527a710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360401"
---
# <a name="iscanprofilegetguid-method"></a><span data-ttu-id="8c326-103">IScanProfile:: GetGUID (método)</span><span class="sxs-lookup"><span data-stu-id="8c326-103">IScanProfile::GetGUID method</span></span>

<span data-ttu-id="8c326-104">Devuelve el GUID del perfil.</span><span class="sxs-lookup"><span data-stu-id="8c326-104">Returns the GUID of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c326-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c326-105">Syntax</span></span>


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a><span data-ttu-id="8c326-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c326-107">*retval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c326-107">*retVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c326-108">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="8c326-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="8c326-109">Puntero al GUID del perfil.</span><span class="sxs-lookup"><span data-stu-id="8c326-109">A pointer to the GUID of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c326-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c326-110">Return value</span></span>

<span data-ttu-id="8c326-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8c326-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8c326-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8c326-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8c326-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c326-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c326-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c326-114">Remarks</span></span>

<span data-ttu-id="8c326-115">El GUID de un perfil se genera automáticamente cuando se crea el perfil con [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span><span class="sxs-lookup"><span data-stu-id="8c326-115">The GUID for a profile is automatically generated when the profile is created with [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c326-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c326-116">Requirements</span></span>



| <span data-ttu-id="8c326-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c326-117">Requirement</span></span> | <span data-ttu-id="8c326-118">Value</span><span class="sxs-lookup"><span data-stu-id="8c326-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c326-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c326-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8c326-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8c326-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8c326-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c326-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8c326-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c326-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c326-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c326-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c326-124"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c326-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="8c326-125">IDL</span><span class="sxs-lookup"><span data-stu-id="8c326-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8c326-126"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8c326-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c326-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c326-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c326-128">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="8c326-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="8c326-129">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="8c326-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




