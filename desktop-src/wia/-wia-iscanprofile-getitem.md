---
description: Obtiene el GUID de la categoría del elemento 2,0 de adquisición de imágenes de Windows (WIA) al que está asociado el perfil.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'IScanProfile:: GetItem (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652475"
---
# <a name="iscanprofilegetitem-method"></a><span data-ttu-id="8c1da-103">IScanProfile:: GetItem (método)</span><span class="sxs-lookup"><span data-stu-id="8c1da-103">IScanProfile::GetItem method</span></span>

<span data-ttu-id="8c1da-104">Obtiene el GUID de la categoría del elemento 2,0 de adquisición de imágenes de Windows (WIA) al que está asociado el perfil.</span><span class="sxs-lookup"><span data-stu-id="8c1da-104">Gets the GUID of the category of the Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c1da-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c1da-105">Syntax</span></span>


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="8c1da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c1da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c1da-107">*pguidCategory* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c1da-107">*pguidCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c1da-108">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="8c1da-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="8c1da-109">Un puntero al GUID de la categoría del elemento de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="8c1da-109">A pointer to the GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="8c1da-110">Siempre es una de las constantes de \_ categoría del elemento IPA de WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8c1da-110">This is always one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c1da-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c1da-111">Return value</span></span>

<span data-ttu-id="8c1da-112">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8c1da-112">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8c1da-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8c1da-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8c1da-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c1da-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c1da-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c1da-115">Requirements</span></span>



| <span data-ttu-id="8c1da-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c1da-116">Requirement</span></span> | <span data-ttu-id="8c1da-117">Value</span><span class="sxs-lookup"><span data-stu-id="8c1da-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c1da-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c1da-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8c1da-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8c1da-119">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8c1da-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c1da-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8c1da-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c1da-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c1da-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c1da-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c1da-123"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c1da-123"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="8c1da-124">IDL</span><span class="sxs-lookup"><span data-stu-id="8c1da-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8c1da-125"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8c1da-125"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c1da-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c1da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c1da-127">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="8c1da-127">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="8c1da-128">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="8c1da-128">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




