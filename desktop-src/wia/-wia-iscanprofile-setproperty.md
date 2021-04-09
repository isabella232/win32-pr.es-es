---
description: Establece el valor de las propiedades secundarias especificadas en el <Properties> elemento de un perfil de digitalización.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'IScanProfile:: SetProperty (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810790"
---
# <a name="iscanprofilesetproperty-method"></a><span data-ttu-id="9fc40-104">IScanProfile:: SetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="9fc40-104">IScanProfile::SetProperty method</span></span>

<span data-ttu-id="9fc40-105">Establece el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de digitalización.</span><span class="sxs-lookup"><span data-stu-id="9fc40-105">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc40-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fc40-106">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="9fc40-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fc40-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc40-108">*número* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9fc40-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc40-109">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="9fc40-109">Type: **ULONG**</span></span>

<span data-ttu-id="9fc40-110">El número de entradas de las matrices a las que apuntan *PID* y *PVAR*.</span><span class="sxs-lookup"><span data-stu-id="9fc40-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="9fc40-111">*PID* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9fc40-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc40-112">Tipo: \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="9fc40-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="9fc40-113">Puntero a una matriz de números de identificación de las propiedades que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="9fc40-113">A pointer to an array of identification numbers of the properties to be set.</span></span> <span data-ttu-id="9fc40-114">Cada valor de la matriz es una [constante de propiedad de WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9fc40-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fc40-115">_pvar \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9fc40-115">_pvar\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc40-116">Tipo: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="9fc40-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="9fc40-117">Puntero a una matriz de valores que se va a asignar a las propiedades.</span><span class="sxs-lookup"><span data-stu-id="9fc40-117">A pointer to an array of values to be assigned to the properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc40-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fc40-118">Return value</span></span>

<span data-ttu-id="9fc40-119">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9fc40-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9fc40-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9fc40-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9fc40-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9fc40-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc40-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fc40-122">Remarks</span></span>

<span data-ttu-id="9fc40-123">Cada valor de la matriz al que apunta el *PID* es una de las [constantes de propiedad de WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9fc40-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="9fc40-124">Puede extender este sistema de identificación.</span><span class="sxs-lookup"><span data-stu-id="9fc40-124">You can extend this identification system.</span></span> <span data-ttu-id="9fc40-125">Vea [definir propiedades personalizadas](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9fc40-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="9fc40-126">Los cambios en un perfil no se guardan en el disco hasta que la aplicación llama al método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc40-126">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="9fc40-127">Si dos aplicaciones crean objetos de Perfil de análisis a partir del mismo archivo XML y cada aplicación escribe cambios en su objeto, solo los cambios realizados por la aplicación que llama a [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last se guardan en el disco.</span><span class="sxs-lookup"><span data-stu-id="9fc40-127">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc40-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fc40-128">Requirements</span></span>



| <span data-ttu-id="9fc40-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fc40-129">Requirement</span></span> | <span data-ttu-id="9fc40-130">Value</span><span class="sxs-lookup"><span data-stu-id="9fc40-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc40-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fc40-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc40-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9fc40-132">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9fc40-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fc40-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc40-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9fc40-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fc40-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fc40-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fc40-136"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fc40-136"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="9fc40-137">IDL</span><span class="sxs-lookup"><span data-stu-id="9fc40-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9fc40-138"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9fc40-138"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc40-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fc40-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc40-140">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="9fc40-140">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="9fc40-141">**Vista**</span><span class="sxs-lookup"><span data-stu-id="9fc40-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9fc40-142">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="9fc40-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="9fc40-143">Constantes de propiedad de WIA</span><span class="sxs-lookup"><span data-stu-id="9fc40-143">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="9fc40-144">Definir propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="9fc40-144">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
