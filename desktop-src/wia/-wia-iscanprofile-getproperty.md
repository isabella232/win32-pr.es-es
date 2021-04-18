---
description: Obtiene el valor de las propiedades secundarias especificadas en el <Properties> elemento de un perfil de digitalización.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'IScanProfile:: GetProperty (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720402"
---
# <a name="iscanprofilegetproperty-method"></a><span data-ttu-id="dabfb-104">IScanProfile:: GetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="dabfb-104">IScanProfile::GetProperty method</span></span>

<span data-ttu-id="dabfb-105">Obtiene el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de digitalización.</span><span class="sxs-lookup"><span data-stu-id="dabfb-105">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="dabfb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dabfb-106">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="dabfb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dabfb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dabfb-108">*número* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="dabfb-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dabfb-109">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="dabfb-109">Type: **ULONG**</span></span>

<span data-ttu-id="dabfb-110">El número de entradas de las matrices a las que apuntan *PID* y *PVAR*.</span><span class="sxs-lookup"><span data-stu-id="dabfb-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="dabfb-111">*PID* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="dabfb-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dabfb-112">Tipo: \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="dabfb-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="dabfb-113">Puntero a una matriz de los números de identificación de las propiedades que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="dabfb-113">A pointer to an array of the identification numbers of the properties to be set.</span></span> <span data-ttu-id="dabfb-114">Cada valor de la matriz es una [constante de propiedad de WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="dabfb-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="dabfb-115">_pvar \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dabfb-115">_pvar\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dabfb-116">Tipo: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="dabfb-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="dabfb-117">Puntero a una matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="dabfb-117">A pointer to an array of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dabfb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dabfb-118">Return value</span></span>

<span data-ttu-id="dabfb-119">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="dabfb-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="dabfb-120">Devuelve S \_ false si alguno de los valores de propiedad no está disponible; de lo contrario, devuelve s \_ OK o un código de error com estándar.</span><span class="sxs-lookup"><span data-stu-id="dabfb-120">Returns S\_FALSE if any of the property values is not available; otherwise, returns S\_OK or a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dabfb-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dabfb-121">Remarks</span></span>

<span data-ttu-id="dabfb-122">El tipo de cada valor debe ser del mismo tipo que se estableció con la llamada a [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="dabfb-122">The type of each value must be the same type that was set with the call to [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).</span></span>

<span data-ttu-id="dabfb-123">Cada valor de la matriz al que apunta el *PID* es una de las [constantes de propiedad de WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="dabfb-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="dabfb-124">Puede extender este sistema de identificación.</span><span class="sxs-lookup"><span data-stu-id="dabfb-124">You can extend this identification system.</span></span> <span data-ttu-id="dabfb-125">Vea [definir propiedades personalizadas](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="dabfb-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dabfb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dabfb-126">Requirements</span></span>



| <span data-ttu-id="dabfb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dabfb-127">Requirement</span></span> | <span data-ttu-id="dabfb-128">Value</span><span class="sxs-lookup"><span data-stu-id="dabfb-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dabfb-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dabfb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dabfb-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dabfb-130">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="dabfb-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dabfb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dabfb-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dabfb-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dabfb-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dabfb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dabfb-134"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="dabfb-134"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="dabfb-135">IDL</span><span class="sxs-lookup"><span data-stu-id="dabfb-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dabfb-136"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dabfb-136"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dabfb-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="dabfb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dabfb-138">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="dabfb-138">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="dabfb-139">**Vista**</span><span class="sxs-lookup"><span data-stu-id="dabfb-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dabfb-140">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="dabfb-140">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="dabfb-141">Constantes de propiedad de WIA</span><span class="sxs-lookup"><span data-stu-id="dabfb-141">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="dabfb-142">Definir propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="dabfb-142">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
