---
description: Abre un perfil de digitalización que se ha guardado en el disco como archivo XML.
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: 'IScanProfileMgr:: OpenProfile (método) (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.OpenProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 40d380a2b0405445cba72a0aac73c4b529114fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716059"
---
# <a name="iscanprofilemgropenprofile-method"></a><span data-ttu-id="9a9f2-103">IScanProfileMgr:: OpenProfile (método)</span><span class="sxs-lookup"><span data-stu-id="9a9f2-103">IScanProfileMgr::OpenProfile method</span></span>

<span data-ttu-id="9a9f2-104">Abre un perfil de digitalización que se ha guardado en el disco como archivo XML.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-104">Opens a scan profile that has been saved to disk as an XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a9f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a9f2-105">Syntax</span></span>


```C++
HRESULT OpenProfile(
  [in]  GUID         guid,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="9a9f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a9f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a9f2-107">*GUID* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9a9f2-107">*guid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9f2-108">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="9a9f2-108">Type: **GUID**</span></span>

<span data-ttu-id="9a9f2-109">GUID del perfil.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-109">The GUID of the profile.</span></span>

</dd> <dt>

<span data-ttu-id="9a9f2-110">*ppScanProfile* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9a9f2-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9f2-111">Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9a9f2-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="9a9f2-112">Dirección de un puntero al perfil.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-112">The address of a pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a9f2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a9f2-113">Return value</span></span>

<span data-ttu-id="9a9f2-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9a9f2-114">Type: **HRESULT**</span></span>

<span data-ttu-id="9a9f2-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a9f2-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a9f2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a9f2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a9f2-117">Remarks</span></span>

<span data-ttu-id="9a9f2-118">Si un perfil de digitalización se guarda con el método [**Save**](-wia-iscanprofile-save.md) , se almacena como un archivo XML en% userprofile% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-118">If a scan profile is saved using the [**Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a9f2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a9f2-119">Requirements</span></span>



| <span data-ttu-id="9a9f2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a9f2-120">Requirement</span></span> | <span data-ttu-id="9a9f2-121">Value</span><span class="sxs-lookup"><span data-stu-id="9a9f2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a9f2-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a9f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9a9f2-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9a9f2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9a9f2-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a9f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9a9f2-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a9f2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a9f2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a9f2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a9f2-127"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a9f2-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="9a9f2-128">IDL</span><span class="sxs-lookup"><span data-stu-id="9a9f2-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a9f2-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a9f2-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a9f2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a9f2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a9f2-131">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="9a9f2-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="9a9f2-132">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="9a9f2-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




