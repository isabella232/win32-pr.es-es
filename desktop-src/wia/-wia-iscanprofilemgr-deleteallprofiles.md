---
description: Elimina todos los perfiles de análisis asociados con el dispositivo especificado.
ms.assetid: 5abf101b-0442-47fc-8159-95db63f0af78
title: IScanProfileMgr::D método eleteAllProfiles (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f21e9f562d008846b4ecf6ad46e86c2c371eb9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082671"
---
# <a name="iscanprofilemgrdeleteallprofiles-method"></a><span data-ttu-id="4a29a-103">IScanProfileMgr::D método eleteAllProfiles</span><span class="sxs-lookup"><span data-stu-id="4a29a-103">IScanProfileMgr::DeleteAllProfiles method</span></span>

<span data-ttu-id="4a29a-104">Elimina todos los perfiles de análisis asociados con el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4a29a-104">Deletes all the scan profiles associated with the specified device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a29a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a29a-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfiles(
  [in] BSTR bstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="4a29a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a29a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a29a-107">*bstrDeviceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4a29a-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a29a-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4a29a-108">Type: **BSTR**</span></span>

<span data-ttu-id="4a29a-109">IDENTIFICADOR del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a29a-109">The ID of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a29a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a29a-110">Return value</span></span>

<span data-ttu-id="4a29a-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a29a-111">Type: **HRESULT**</span></span>

<span data-ttu-id="4a29a-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4a29a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a29a-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a29a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a29a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a29a-114">Requirements</span></span>



| <span data-ttu-id="4a29a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a29a-115">Requirement</span></span> | <span data-ttu-id="4a29a-116">Value</span><span class="sxs-lookup"><span data-stu-id="4a29a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a29a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a29a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a29a-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4a29a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4a29a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a29a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a29a-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a29a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a29a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a29a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a29a-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a29a-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="4a29a-123">IDL</span><span class="sxs-lookup"><span data-stu-id="4a29a-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a29a-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a29a-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a29a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a29a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a29a-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="4a29a-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="4a29a-127">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="4a29a-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




