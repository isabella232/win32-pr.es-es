---
title: Método IWMDRMLicenseQuery QueryLicenseState (wmdrmsdk. h)
description: El método QueryLicenseState consulta el almacén de licencias local para obtener la información de licencia que se aplica a un identificador de clave para uno o más derechos específicos.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Método QueryLicenseState formato de Windows Media
- Método QueryLicenseState formato de Windows Media, interfaz IWMDRMLicenseQuery
- Interfaz IWMDRMLicenseQuery formato de Windows Media, método QueryLicenseState
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699338"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a><span data-ttu-id="8fff2-106">IWMDRMLicenseQuery:: QueryLicenseState (método)</span><span class="sxs-lookup"><span data-stu-id="8fff2-106">IWMDRMLicenseQuery::QueryLicenseState method</span></span>

<span data-ttu-id="8fff2-107">El método **QueryLicenseState** consulta el almacén de licencias local para obtener la información de licencia que se aplica a un identificador de clave para uno o más derechos específicos.</span><span class="sxs-lookup"><span data-stu-id="8fff2-107">The **QueryLicenseState** method queries the local license store for license information that applies to a Key ID for one or more specific rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fff2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fff2-108">Syntax</span></span>


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a><span data-ttu-id="8fff2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fff2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fff2-110">*bstrKID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fff2-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fff2-111">IDENTIFICADOR de clave que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="8fff2-111">Key ID for which to query.</span></span> <span data-ttu-id="8fff2-112">Solo se evaluarán las licencias que se apliquen a este ID. de clave.</span><span class="sxs-lookup"><span data-stu-id="8fff2-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="8fff2-113">*cActionsToQuery* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fff2-113">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fff2-114">Número de acciones que se van a consultar.</span><span class="sxs-lookup"><span data-stu-id="8fff2-114">The number of actions for which to query.</span></span> <span data-ttu-id="8fff2-115">Este valor debe establecerse en el número de elementos de las matrices que se pasan para los parámetros *rgbstrActionsToQuery* y *rgResultStateData* .</span><span class="sxs-lookup"><span data-stu-id="8fff2-115">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgResultStateData* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="8fff2-116">*\[ rgbstrActionsToQuery \]* \[en\]</span><span class="sxs-lookup"><span data-stu-id="8fff2-116">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fff2-117">Matriz de uno o más derechos que se van a consultar.</span><span class="sxs-lookup"><span data-stu-id="8fff2-117">Array of one or more rights for which to query.</span></span> <span data-ttu-id="8fff2-118">Esta matriz debe contener tantos elementos como especifique el *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="8fff2-118">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="8fff2-119">Cada elemento debe establecerse en una de las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="8fff2-119">Each element must be set to one of the following constants.</span></span>



| <span data-ttu-id="8fff2-120">Constante</span><span class="sxs-lookup"><span data-stu-id="8fff2-120">Constant</span></span>                                        | <span data-ttu-id="8fff2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fff2-121">Description</span></span>                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fff2-122">g \_ wszWMDRM \_ LicenseState \_ backup</span><span class="sxs-lookup"><span data-stu-id="8fff2-122">g\_wszWMDRM\_LicenseState\_Backup</span></span>               | <span data-ttu-id="8fff2-123">Incluir para consultar los detalles sobre el derecho a realizar una copia de seguridad y restaurar la licencia.</span><span class="sxs-lookup"><span data-stu-id="8fff2-123">Include to query for the details about the right to back up and restore the license.</span></span>                                                               |
| <span data-ttu-id="8fff2-124">g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="8fff2-124">g\_wszWMDRM\_LicenseState\_CollaborativePlay</span></span>    | <span data-ttu-id="8fff2-125">Incluir para consultar los detalles sobre el derecho a compartir el contenido con un grupo de usuarios como parte de un escenario de reproducción colaborativa.</span><span class="sxs-lookup"><span data-stu-id="8fff2-125">Include to query for the details about the right to share the content with a group of users as part of a collaborative playback scenario.</span></span>          |
| <span data-ttu-id="8fff2-126">g \_ wszWMDRM \_ LicenseState \_</span><span class="sxs-lookup"><span data-stu-id="8fff2-126">g\_wszWMDRM\_LicenseState\_Copy</span></span>                 | <span data-ttu-id="8fff2-127">Incluir para consultar los detalles sobre el derecho a copiar el contenido en dispositivos o medios externos.</span><span class="sxs-lookup"><span data-stu-id="8fff2-127">Include to query for the details about the right to copy the content to external devices or media.</span></span>                                                 |
| <span data-ttu-id="8fff2-128">g \_ wszWMDRM \_ LicenseState \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="8fff2-128">g\_wszWMDRM\_LicenseState\_CopyToCD</span></span>             | <span data-ttu-id="8fff2-129">Incluir para consultar los detalles sobre la derecha para copiar el contenido en un CD.</span><span class="sxs-lookup"><span data-stu-id="8fff2-129">Include to query for the details about the right to copy the content to CD.</span></span>                                                                        |
| <span data-ttu-id="8fff2-130">g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="8fff2-130">g\_wszWMDRM\_LicenseState\_CopyToNonSDMIDevice</span></span>  | <span data-ttu-id="8fff2-131">Incluir para consultar los detalles sobre la derecha para copiar el contenido en un dispositivo que no admita la iniciativa de medios digitales seguros (SDMI).</span><span class="sxs-lookup"><span data-stu-id="8fff2-131">Include to query for the details about the right to copy the content to a device that does not support the secure digital media initiative (SDMI).</span></span> |
| <span data-ttu-id="8fff2-132">g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="8fff2-132">g\_wszWMDRM\_LicenseState\_CopyToSDMIDevice</span></span>     | <span data-ttu-id="8fff2-133">Incluir para consultar los detalles sobre la derecha para copiar el contenido en un dispositivo compatible con SDMI.</span><span class="sxs-lookup"><span data-stu-id="8fff2-133">Include to query for the details about the right to copy the content to a device that supports the SDMI.</span></span>                                           |
| <span data-ttu-id="8fff2-134">g \_ wszWMDRM \_ LicenseState \_ CreateThumbnailImage</span><span class="sxs-lookup"><span data-stu-id="8fff2-134">g\_wszWMDRM\_LicenseState\_CreateThumbnailImage</span></span> | <span data-ttu-id="8fff2-135">Incluir para consultar los detalles sobre la derecha para crear una imagen en miniatura a partir del contenido.</span><span class="sxs-lookup"><span data-stu-id="8fff2-135">Include to query for the details about the right to create a thumbnail image from the content.</span></span>                                                     |
| <span data-ttu-id="8fff2-136">g \_ wszWMDRM \_ LicenseState \_ reproducción</span><span class="sxs-lookup"><span data-stu-id="8fff2-136">g\_wszWMDRM\_LicenseState\_Playback</span></span>             | <span data-ttu-id="8fff2-137">Incluir para consultar los detalles sobre el derecho a reproducir el contenido.</span><span class="sxs-lookup"><span data-stu-id="8fff2-137">Include to query for the details about the right to play the content.</span></span>                                                                              |
| <span data-ttu-id="8fff2-138">g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn</span><span class="sxs-lookup"><span data-stu-id="8fff2-138">g\_wszWMDRM\_LicenseState\_PlaylistBurn</span></span>         | <span data-ttu-id="8fff2-139">Incluir para consultar los detalles sobre la derecha para copiar el contenido en CD como parte de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="8fff2-139">Include to query for the details about the right to copy the content to CD as part of a playlist.</span></span>                                                  |



 

</dd> <dt>

<span data-ttu-id="8fff2-140">*\[ rgResultStateData \]* \[fuera de\]</span><span class="sxs-lookup"><span data-stu-id="8fff2-140">*rgResultStateData\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fff2-141">Matriz de una o varias estructuras de datos de estado de la [**\_ licencia \_ \_ DRM**](drmdrm-license-state-data.md) que reciben la información de estado de la licencia que se aplica a la derecha en el elemento correspondiente del parámetro *rgbstrActionsToQuery* .</span><span class="sxs-lookup"><span data-stu-id="8fff2-141">Array of one or more [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structures that receive the license state information that applies to the right in the corresponding element of the *rgbstrActionsToQuery* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fff2-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fff2-142">Return value</span></span>

<span data-ttu-id="8fff2-143">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8fff2-143">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8fff2-144">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="8fff2-144">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8fff2-145">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8fff2-145">Return code</span></span>                                                                          | <span data-ttu-id="8fff2-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fff2-146">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8fff2-147"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8fff2-147"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8fff2-148">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="8fff2-148">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8fff2-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fff2-149">Remarks</span></span>

<span data-ttu-id="8fff2-150">Se buscarán y evaluarán todas las licencias que se aplican al identificador de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="8fff2-150">All licenses that apply to the specified Key ID will be searched and evaluated.</span></span> <span data-ttu-id="8fff2-151">Los resultados se agregan, por lo que cada estructura de **\_ datos de \_ estado \_ de licencia DRM** puede contener información de varias licencias.</span><span class="sxs-lookup"><span data-stu-id="8fff2-151">The results are aggregated, so each **DRM\_LICENSE\_STATE\_DATA** structure may contain information from multiple licenses.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fff2-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fff2-152">Requirements</span></span>



| <span data-ttu-id="8fff2-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fff2-153">Requirement</span></span> | <span data-ttu-id="8fff2-154">Value</span><span class="sxs-lookup"><span data-stu-id="8fff2-154">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fff2-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fff2-155">Header</span></span><br/>  | <dl> <span data-ttu-id="8fff2-156"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fff2-156"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8fff2-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8fff2-157">Library</span></span><br/> | <dl> <span data-ttu-id="8fff2-158"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fff2-158"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fff2-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fff2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fff2-160">**Interfaz IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="8fff2-160">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> </dl>

 

 





