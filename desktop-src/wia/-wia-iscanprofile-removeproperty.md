---
description: Quita una lista especificada de propiedades secundarias en el <Properties> elemento de un perfil de digitalización.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'IScanProfile:: RemoveProperty (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154872"
---
# <a name="iscanprofileremoveproperty-method"></a><span data-ttu-id="a98ac-104">IScanProfile:: RemoveProperty (método)</span><span class="sxs-lookup"><span data-stu-id="a98ac-104">IScanProfile::RemoveProperty method</span></span>

<span data-ttu-id="a98ac-105">Quita una lista especificada de propiedades secundarias en el `<Properties>` elemento de un perfil de digitalización.</span><span class="sxs-lookup"><span data-stu-id="a98ac-105">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="a98ac-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a98ac-106">Syntax</span></span>


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a><span data-ttu-id="a98ac-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a98ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a98ac-108">*número* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a98ac-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a98ac-109">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="a98ac-109">Type: **ULONG**</span></span>

<span data-ttu-id="a98ac-110">Número de entradas de la matriz a la que señala el *PID* .</span><span class="sxs-lookup"><span data-stu-id="a98ac-110">The number of entries in the array that *pid* points to.</span></span>

</dd> <dt>

<span data-ttu-id="a98ac-111">*PID* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a98ac-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a98ac-112">Tipo: \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="a98ac-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="a98ac-113">Puntero a una matriz de números de identificación de las propiedades que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="a98ac-113">A pointer to an array of identification numbers of the properties to be deleted.</span></span> <span data-ttu-id="a98ac-114">Cada una de ellas es una [constante de propiedad de WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a98ac-114">Each is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a98ac-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a98ac-115">Return value</span></span>

<span data-ttu-id="a98ac-116">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a98ac-116">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a98ac-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a98ac-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a98ac-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a98ac-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a98ac-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a98ac-119">Remarks</span></span>

<span data-ttu-id="a98ac-120">Cada valor de la matriz al que apunta el *PID* es una de las [constantes de propiedad de WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a98ac-120">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="a98ac-121">Puede extender este sistema de identificación.</span><span class="sxs-lookup"><span data-stu-id="a98ac-121">You can extend this identification system.</span></span> <span data-ttu-id="a98ac-122">Vea [definir propiedades personalizadas](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a98ac-122">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="a98ac-123">Los cambios en un perfil no se guardan en el disco hasta que la aplicación llama al método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="a98ac-123">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="a98ac-124">Si dos aplicaciones crean objetos de Perfil de análisis a partir del mismo archivo XML y cada aplicación escribe cambios en su objeto, solo los cambios realizados por la aplicación que llama a [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last se guardan en el disco.</span><span class="sxs-lookup"><span data-stu-id="a98ac-124">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="a98ac-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a98ac-125">Requirements</span></span>



| <span data-ttu-id="a98ac-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a98ac-126">Requirement</span></span> | <span data-ttu-id="a98ac-127">Value</span><span class="sxs-lookup"><span data-stu-id="a98ac-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a98ac-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a98ac-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a98ac-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a98ac-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a98ac-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a98ac-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a98ac-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a98ac-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a98ac-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a98ac-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a98ac-133"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="a98ac-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="a98ac-134">IDL</span><span class="sxs-lookup"><span data-stu-id="a98ac-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a98ac-135"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a98ac-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a98ac-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a98ac-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a98ac-137">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="a98ac-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="a98ac-138">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a98ac-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a98ac-139">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="a98ac-139">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="a98ac-140">Constantes de propiedad de WIA</span><span class="sxs-lookup"><span data-stu-id="a98ac-140">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="a98ac-141">Definir propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="a98ac-141">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 




