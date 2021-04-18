---
description: Establece el GUID de la categoría del elemento 2,0 de adquisición de imágenes de Windows (WIA) al que está asociado el perfil.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'IScanProfile:: SetItem (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715351"
---
# <a name="iscanprofilesetitem-method"></a><span data-ttu-id="e3b8e-103">IScanProfile:: SetItem (método)</span><span class="sxs-lookup"><span data-stu-id="e3b8e-103">IScanProfile::SetItem method</span></span>

<span data-ttu-id="e3b8e-104">Establece el GUID de la categoría del elemento 2,0 de adquisición de imágenes de Windows (WIA) al que está asociado el perfil.</span><span class="sxs-lookup"><span data-stu-id="e3b8e-104">Sets the GUID of the category of Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b8e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3b8e-105">Syntax</span></span>


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="e3b8e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3b8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b8e-107">*guidCategory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3b8e-107">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b8e-108">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="e3b8e-108">Type: **GUID**</span></span>

<span data-ttu-id="e3b8e-109">El GUID de la categoría del elemento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="e3b8e-109">The GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="e3b8e-110">Debe ser una de las constantes de \_ categoría de elemento IPA de WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e3b8e-110">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b8e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3b8e-111">Return value</span></span>

<span data-ttu-id="e3b8e-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e3b8e-112">Type: **HRESULT**</span></span>

<span data-ttu-id="e3b8e-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e3b8e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3b8e-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3b8e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b8e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3b8e-115">Remarks</span></span>

<span data-ttu-id="e3b8e-116">Los usuarios pueden cambiar la categoría con el método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="e3b8e-116">Users can change the category with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="e3b8e-117">Los cambios en un perfil no se guardan en el disco hasta que la aplicación llama al método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="e3b8e-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="e3b8e-118">Si dos aplicaciones crean objetos de Perfil de análisis a partir del mismo archivo XML y cada aplicación escribe cambios en su objeto, solo los cambios realizados por la aplicación que llama a [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last se guardan en el disco.</span><span class="sxs-lookup"><span data-stu-id="e3b8e-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b8e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3b8e-119">Requirements</span></span>



| <span data-ttu-id="e3b8e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b8e-120">Requirement</span></span> | <span data-ttu-id="e3b8e-121">Value</span><span class="sxs-lookup"><span data-stu-id="e3b8e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b8e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3b8e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e3b8e-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e3b8e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e3b8e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3b8e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e3b8e-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3b8e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3b8e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3b8e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3b8e-127"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b8e-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="e3b8e-128">IDL</span><span class="sxs-lookup"><span data-stu-id="e3b8e-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3b8e-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3b8e-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b8e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3b8e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b8e-131">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="e3b8e-131">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="e3b8e-132">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="e3b8e-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




