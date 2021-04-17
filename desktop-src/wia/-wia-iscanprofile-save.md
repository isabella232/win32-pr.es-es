---
description: Guarda los cambios en un perfil en el disco.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'IScanProfile:: Save (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542806"
---
# <a name="iscanprofilesave-method"></a><span data-ttu-id="56572-103">IScanProfile:: Save (método)</span><span class="sxs-lookup"><span data-stu-id="56572-103">IScanProfile::Save method</span></span>

<span data-ttu-id="56572-104">Guarda los cambios en un perfil en el disco.</span><span class="sxs-lookup"><span data-stu-id="56572-104">Saves changes to a profile to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="56572-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56572-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="56572-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56572-106">Parameters</span></span>

<span data-ttu-id="56572-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="56572-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56572-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56572-108">Return value</span></span>

<span data-ttu-id="56572-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="56572-109">Type: **HRESULT**</span></span>

<span data-ttu-id="56572-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="56572-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56572-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56572-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="56572-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56572-112">Remarks</span></span>

<span data-ttu-id="56572-113">Un perfil de digitalización guardado es un archivo XML almacenado en% USERPROFILE% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="56572-113">A saved scan profile is an XML file stored at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="56572-114">Si más de un proceso escribe en el objeto [**IScanProfile**](-wia-iscanprofile.md) , el que llama a **IScanProfile:: Save** Last es el único proceso cuyos cambios se guardan.</span><span class="sxs-lookup"><span data-stu-id="56572-114">If more than one process writes to the [**IScanProfile**](-wia-iscanprofile.md) object, the one that calls **IScanProfile::Save** last is the only process whose changes are saved.</span></span>

<span data-ttu-id="56572-115">El método **IScanProfile:: Save** valida el perfil antes de guardarlo.</span><span class="sxs-lookup"><span data-stu-id="56572-115">The **IScanProfile::Save** method validates the profile before saving.</span></span> <span data-ttu-id="56572-116">El perfil siempre se considera válido a menos que la categoría del elemento 2,0 de adquisición de imágenes de Windows (WIA) asociada al perfil sea el alimentador de la categoría WIA \_ \_ o el \_ alimentador de la categoría WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="56572-116">The profile is always considered valid unless the category of the Windows Image Acquisition (WIA) 2.0 item associated with the profile is either WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER.</span></span> <span data-ttu-id="56572-117">Si la categoría es la \_ categoría \_ de WIA plana o el \_ \_ alimentador de la categoría WIA, las siguientes propiedades deben ser válidas para el elemento, si las propiedades están contenidas en el perfil:</span><span class="sxs-lookup"><span data-stu-id="56572-117">If the category is WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER, the following properties must be valid for the item, if the properties are contained in the profile:</span></span>

<span data-ttu-id="56572-118">\_brillo de IP de WIA \_</span><span class="sxs-lookup"><span data-stu-id="56572-118">WIA\_IPS\_BRIGHTNESS</span></span>

<span data-ttu-id="56572-119">\_contraste de IP de WIA \_</span><span class="sxs-lookup"><span data-stu-id="56572-119">WIA\_IPS\_CONTRAST</span></span>

<span data-ttu-id="56572-120">tipo de DataType del \_ IPA de WIA \_</span><span class="sxs-lookup"><span data-stu-id="56572-120">WIA\_IPA\_DATATYPE</span></span>

<span data-ttu-id="56572-121">\_XRES de IP WIA \_</span><span class="sxs-lookup"><span data-stu-id="56572-121">WIA\_IPS\_XRES</span></span>

<span data-ttu-id="56572-122">\_formato de IPA de WIA \_</span><span class="sxs-lookup"><span data-stu-id="56572-122">WIA\_IPA\_FORMAT</span></span>

<span data-ttu-id="56572-123">Además, si la categoría es \_ alimentador de categoría WIA \_ , la \_ propiedad tamaño de página de IPS de WIA \_ \_ debe ser válida, si está presente en el perfil.</span><span class="sxs-lookup"><span data-stu-id="56572-123">In addition, if the category is WIA\_CATEGORY\_FEEDER, the WIA\_IPS\_PAGE\_SIZE property must be valid, if it is present in the profile.</span></span> <span data-ttu-id="56572-124">Para obtener más información sobre estas propiedades, consulte el artículo sobre las constantes de las propiedades de los [**elementos de WIA**](-wia-wiaitempropscanneritem.md).</span><span class="sxs-lookup"><span data-stu-id="56572-124">For more information about these properties, see [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56572-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56572-125">Requirements</span></span>



| <span data-ttu-id="56572-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="56572-126">Requirement</span></span> | <span data-ttu-id="56572-127">Value</span><span class="sxs-lookup"><span data-stu-id="56572-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="56572-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56572-128">Minimum supported client</span></span><br/> | <span data-ttu-id="56572-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56572-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="56572-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56572-130">Minimum supported server</span></span><br/> | <span data-ttu-id="56572-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="56572-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56572-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56572-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="56572-133"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="56572-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="56572-134">IDL</span><span class="sxs-lookup"><span data-stu-id="56572-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56572-135"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56572-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56572-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="56572-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56572-137">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="56572-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="56572-138">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="56572-138">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




