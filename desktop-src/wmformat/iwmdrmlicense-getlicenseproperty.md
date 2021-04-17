---
title: Método IWMDRMLicense GetLicenseProperty (wmdrmsdk. h)
description: El método GetLicenseProperty recupera una propiedad de la licencia actual.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Método GetLicenseProperty formato de Windows Media
- Método GetLicenseProperty formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetLicenseProperty
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708265"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a><span data-ttu-id="3e2a3-106">IWMDRMLicense:: GetLicenseProperty (método)</span><span class="sxs-lookup"><span data-stu-id="3e2a3-106">IWMDRMLicense::GetLicenseProperty method</span></span>

<span data-ttu-id="3e2a3-107">El método **GetLicenseProperty** recupera una propiedad de la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-107">The **GetLicenseProperty** method retrieves a property from the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e2a3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e2a3-108">Syntax</span></span>


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a><span data-ttu-id="3e2a3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e2a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e2a3-110">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e2a3-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2a3-111">Nombre de la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-111">Name of the property to retrieve.</span></span> <span data-ttu-id="3e2a3-112">Establezca en una de las constantes de la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="3e2a3-112">Set to one of the constants in the following table:</span></span>



| <span data-ttu-id="3e2a3-113">Constante</span><span class="sxs-lookup"><span data-stu-id="3e2a3-113">Constant</span></span>                   | <span data-ttu-id="3e2a3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e2a3-114">Description</span></span>                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e2a3-115">g \_ \_ revocación de wszWMDRMNet</span><span class="sxs-lookup"><span data-stu-id="3e2a3-115">g\_wszWMDRMNet\_Revocation</span></span> | <span data-ttu-id="3e2a3-116">Use para obtener la lista de revocación de Windows Media DRM para dispositivos de red para la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-116">Use to get the Windows Media DRM for Network Devices revocation list for the current license.</span></span>                        |
| <span data-ttu-id="3e2a3-117">g \_ wszWMDRM \_ SAPLEVEL</span><span class="sxs-lookup"><span data-stu-id="3e2a3-117">g\_wszWMDRM\_SAPLEVEL</span></span>      | <span data-ttu-id="3e2a3-118">Use para obtener el nivel de la ruta de acceso de audio seguro (SAP) necesario para reproducir el contenido incluido en la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-118">Use to get the Secure Audio Path (SAP) level required to play content covered by the current license.</span></span>                |
| <span data-ttu-id="3e2a3-119">g \_ wszWMDRM \_ SAPRequired</span><span class="sxs-lookup"><span data-stu-id="3e2a3-119">g\_wszWMDRM\_SAPRequired</span></span>   | <span data-ttu-id="3e2a3-120">Use para determinar si la licencia actual requiere que SAP se use para reproducir el contenido.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-120">Use to ascertain whether the current license requires SAP be used to play the content.</span></span>                               |
| <span data-ttu-id="3e2a3-121">g \_ wszWMDRM \_ SOURCEID</span><span class="sxs-lookup"><span data-stu-id="3e2a3-121">g\_wszWMDRM\_SOURCEID</span></span>      | <span data-ttu-id="3e2a3-122">Use para obtener el identificador de origen de la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-122">Use to get the source identifier for the current license.</span></span>                                                            |
| <span data-ttu-id="3e2a3-123">prioridad de g \_ wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="3e2a3-123">g\_wszWMDRM\_PRIORITY</span></span>      | <span data-ttu-id="3e2a3-124">Utilice para obtener la prioridad de la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-124">Use to get the priority of the current license.</span></span> <span data-ttu-id="3e2a3-125">Las licencias de prioridad más alta se aplican antes que las licencias de menor prioridad.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-125">Higher priority licenses are applied before lower priority licenses.</span></span> |
| <span data-ttu-id="3e2a3-126">g \_ wszWMDRM \_ UplinkID</span><span class="sxs-lookup"><span data-stu-id="3e2a3-126">g\_wszWMDRM\_UplinkID</span></span>      | <span data-ttu-id="3e2a3-127">Use para obtener el identificador de clave de la licencia raíz en la cadena de licencias a la que pertenece la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-127">Use to get the key ID of the root license in the license chain that the current license belongs to.</span></span>                  |



 

</dd> <dt>

<span data-ttu-id="3e2a3-128">*ppropVariant* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3e2a3-128">*ppropVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2a3-129">Recibe el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-129">Receives the property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e2a3-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e2a3-130">Return value</span></span>

<span data-ttu-id="3e2a3-131">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-131">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3e2a3-132">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-132">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3e2a3-133">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3e2a3-133">Return code</span></span>                                                                          | <span data-ttu-id="3e2a3-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e2a3-134">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3e2a3-135"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3e2a3-135"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3e2a3-136">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-136">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e2a3-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e2a3-137">Remarks</span></span>

<span data-ttu-id="3e2a3-138">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3e2a3-138">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e2a3-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e2a3-139">Requirements</span></span>



| <span data-ttu-id="3e2a3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e2a3-140">Requirement</span></span> | <span data-ttu-id="3e2a3-141">Value</span><span class="sxs-lookup"><span data-stu-id="3e2a3-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e2a3-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e2a3-142">Header</span></span><br/>  | <dl> <span data-ttu-id="3e2a3-143"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e2a3-143"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e2a3-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e2a3-144">Library</span></span><br/> | <dl> <span data-ttu-id="3e2a3-145"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e2a3-145"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e2a3-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e2a3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2a3-147">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="3e2a3-147">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)
</dt> <dt>

[<span data-ttu-id="3e2a3-148">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="3e2a3-148">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





