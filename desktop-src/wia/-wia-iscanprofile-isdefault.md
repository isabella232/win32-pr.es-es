---
description: Obtiene un valor que indica si el perfil es el perfil de detección predeterminado de un dispositivo IWiaItem2 asociado.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'IScanProfile:: IsDefault (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001303"
---
# <a name="iscanprofileisdefault-method"></a><span data-ttu-id="fef1a-103">IScanProfile:: IsDefault (método)</span><span class="sxs-lookup"><span data-stu-id="fef1a-103">IScanProfile::IsDefault method</span></span>

<span data-ttu-id="fef1a-104">Obtiene un valor que indica si el perfil es el perfil de detección predeterminado de un dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) asociado.</span><span class="sxs-lookup"><span data-stu-id="fef1a-104">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef1a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fef1a-105">Syntax</span></span>


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a><span data-ttu-id="fef1a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fef1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fef1a-107">*pbDefault* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fef1a-107">*pbDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fef1a-108">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="fef1a-108">Type: \**BOOL\** _</span></span>

<span data-ttu-id="fef1a-109">Un puntero a un _ \* BOOL \* \*.</span><span class="sxs-lookup"><span data-stu-id="fef1a-109">A pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="fef1a-110"><span id="TRUE"></span><span id="true"></span>**REALES**</span><span class="sxs-lookup"><span data-stu-id="fef1a-110"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="fef1a-111">El perfil es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fef1a-111">The profile is the default.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="fef1a-112"><span id="FALSE"></span><span id="false"></span>**ES**</span><span class="sxs-lookup"><span data-stu-id="fef1a-112"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="fef1a-113">El perfil no es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fef1a-113">The profile is not the default.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fef1a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fef1a-114">Return value</span></span>

<span data-ttu-id="fef1a-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fef1a-115">Type: **HRESULT**</span></span>

<span data-ttu-id="fef1a-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="fef1a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fef1a-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fef1a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fef1a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fef1a-118">Remarks</span></span>

<span data-ttu-id="fef1a-119">*pbDefault* es **true** si el perfil contiene un `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="fef1a-119">*pbDefault* is **TRUE** if the profile contains a `<Default>` element.</span></span> <span data-ttu-id="fef1a-120">Es **false** si no existe ningún elemento de este tipo.</span><span class="sxs-lookup"><span data-stu-id="fef1a-120">It is **FALSE** if no such element is present.</span></span> <span data-ttu-id="fef1a-121">El elemento no tiene ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fef1a-121">The element has no value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fef1a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fef1a-122">Requirements</span></span>



| <span data-ttu-id="fef1a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fef1a-123">Requirement</span></span> | <span data-ttu-id="fef1a-124">Value</span><span class="sxs-lookup"><span data-stu-id="fef1a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef1a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fef1a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fef1a-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fef1a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="fef1a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fef1a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fef1a-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fef1a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fef1a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fef1a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fef1a-130"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="fef1a-130"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="fef1a-131">IDL</span><span class="sxs-lookup"><span data-stu-id="fef1a-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fef1a-132"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fef1a-132"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fef1a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="fef1a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef1a-134">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="fef1a-134">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="fef1a-135">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="fef1a-135">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




