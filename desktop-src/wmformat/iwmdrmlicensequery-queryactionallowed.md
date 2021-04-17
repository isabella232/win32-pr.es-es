---
title: Método IWMDRMLicenseQuery QueryActionAllowed (wmdrmsdk. h)
description: El método QueryActionAllowed realiza una consulta en el almacén de licencias local para recuperar el estado de la licencia de una o varias acciones DRM que se aplican a un identificador de clave especificado.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Método QueryActionAllowed formato de Windows Media
- Método QueryActionAllowed formato de Windows Media, interfaz IWMDRMLicenseQuery
- Interfaz IWMDRMLicenseQuery formato de Windows Media, método QueryActionAllowed
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680445"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a><span data-ttu-id="0d968-106">IWMDRMLicenseQuery:: QueryActionAllowed (método)</span><span class="sxs-lookup"><span data-stu-id="0d968-106">IWMDRMLicenseQuery::QueryActionAllowed method</span></span>

<span data-ttu-id="0d968-107">El método **QueryActionAllowed** realiza una consulta en el almacén de licencias local para recuperar el estado de la licencia de una o varias acciones DRM que se aplican a un identificador de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="0d968-107">The **QueryActionAllowed** method performs a query on the local license store to retrieve the license status for one or more DRM actions that apply to a specified Key ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d968-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d968-108">Syntax</span></span>


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="0d968-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d968-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d968-110">*bstrKID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d968-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d968-111">IDENTIFICADOR de clave que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="0d968-111">Key ID for which to query.</span></span> <span data-ttu-id="0d968-112">Solo se evaluarán las licencias que se apliquen a este ID. de clave.</span><span class="sxs-lookup"><span data-stu-id="0d968-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="0d968-113">*bstrMinReqIndivVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d968-113">*bstrMinReqIndivVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d968-114">La versión de seguridad mínima especificada en el encabezado del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="0d968-114">The minimum security version specified in the header of the ASF file.</span></span> <span data-ttu-id="0d968-115">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="0d968-115">This parameter is optional.</span></span> <span data-ttu-id="0d968-116">Pase **null** para realizar la consulta sin esta información.</span><span class="sxs-lookup"><span data-stu-id="0d968-116">Pass **NULL** to perform the query without this information.</span></span>

</dd> <dt>

<span data-ttu-id="0d968-117">*cActionsToQuery* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d968-117">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d968-118">Número de acciones que se van a consultar.</span><span class="sxs-lookup"><span data-stu-id="0d968-118">The number of actions for which to query.</span></span> <span data-ttu-id="0d968-119">Este valor debe establecerse en el número de elementos de las matrices que se pasan para los parámetros *rgbstrActionsToQuery* y *rgdwQueryResult* .</span><span class="sxs-lookup"><span data-stu-id="0d968-119">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgdwQueryResult* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="0d968-120">*\[ rgbstrActionsToQuery \]* \[en\]</span><span class="sxs-lookup"><span data-stu-id="0d968-120">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d968-121">Matriz de uno o más derechos que se van a consultar.</span><span class="sxs-lookup"><span data-stu-id="0d968-121">Array of one or more rights for which to query.</span></span> <span data-ttu-id="0d968-122">Esta matriz debe contener tantos elementos como especifique el *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="0d968-122">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="0d968-123">Cada elemento debe establecerse en una de las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="0d968-123">Each element must be set to one of the following constants:</span></span>



| <span data-ttu-id="0d968-124">Constante</span><span class="sxs-lookup"><span data-stu-id="0d968-124">Constant</span></span>                                         | <span data-ttu-id="0d968-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d968-125">Description</span></span>                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0d968-126">g \_ wszWMDRM \_ ActionAllowed \_ reproducción</span><span class="sxs-lookup"><span data-stu-id="0d968-126">g\_wszWMDRM\_ActionAllowed\_Playback</span></span>             | <span data-ttu-id="0d968-127">Incluir para consultar el derecho a reproducir el contenido.</span><span class="sxs-lookup"><span data-stu-id="0d968-127">Include to query for the right to play the content.</span></span>                              |
| <span data-ttu-id="0d968-128">g \_ wszWMDRM \_ ActionAllowed \_</span><span class="sxs-lookup"><span data-stu-id="0d968-128">g\_wszWMDRM\_ActionAllowed\_Copy</span></span>                 | <span data-ttu-id="0d968-129">Incluir para consultar el derecho a copiar el contenido en dispositivos o medios externos.</span><span class="sxs-lookup"><span data-stu-id="0d968-129">Include to query for the right to copy the content to external devices or media.</span></span> |
| <span data-ttu-id="0d968-130">g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn</span><span class="sxs-lookup"><span data-stu-id="0d968-130">g\_wszWMDRM\_ActionAllowed\_PlaylistBurn</span></span>         | <span data-ttu-id="0d968-131">Incluir para consultar el derecho a copiar el contenido en CD como parte de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="0d968-131">Include to query for the right to copy the content to CD as part of a playlist.</span></span>  |
| <span data-ttu-id="0d968-132">g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage</span><span class="sxs-lookup"><span data-stu-id="0d968-132">g\_wszWMDRM\_ActionAllowed\_CreateThumbnailImage</span></span> | <span data-ttu-id="0d968-133">Incluir para consultar el derecho a crear una imagen en miniatura a partir del contenido.</span><span class="sxs-lookup"><span data-stu-id="0d968-133">Include to query for the right to create a thumbnail image from the content.</span></span>     |
| <span data-ttu-id="0d968-134">g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="0d968-134">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>             | <span data-ttu-id="0d968-135">Incluir para consultar el derecho a copiar el contenido en el CD.</span><span class="sxs-lookup"><span data-stu-id="0d968-135">Include to query for the right to copy the content to CD.</span></span>                        |



 

</dd> <dt>

<span data-ttu-id="0d968-136">*\[ rgdwQueryResult \]* \[fuera de\]</span><span class="sxs-lookup"><span data-stu-id="0d968-136">*rgdwQueryResult\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d968-137">Matriz de una o varias variables DWORD que reciben los resultados de la consulta para los derechos especificados por *rgbstrActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="0d968-137">Array of one or more DWORD variables that receive the results of the query for the rights specified by *rgbstrActionsToQuery*.</span></span> <span data-ttu-id="0d968-138">Si se permite una acción, el elemento correspondiente se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="0d968-138">If an action is allowed, the corresponding element is set to zero.</span></span> <span data-ttu-id="0d968-139">Si no se permite una acción, el elemento se establece en uno o más valores de la enumeración de [**\_ \_ \_ \_ resultados de consulta permitidos de la acción DRM**](drm-action-allowed-query-results.md) combinados mediante la operación OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="0d968-139">If an action is not allowed, the element is set to one or more values of the [**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**](drm-action-allowed-query-results.md) enumeration combined by using the bitwise OR operation.</span></span> <span data-ttu-id="0d968-140">Esta matriz debe contener tantos elementos como especifique el *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="0d968-140">This array must contain as many elements as specified by *cActionsToQuery*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d968-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d968-141">Return value</span></span>

<span data-ttu-id="0d968-142">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0d968-142">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0d968-143">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="0d968-143">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0d968-144">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0d968-144">Return code</span></span>                                                                          | <span data-ttu-id="0d968-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d968-145">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0d968-146"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0d968-146"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0d968-147">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="0d968-147">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d968-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d968-148">Remarks</span></span>

<span data-ttu-id="0d968-149">Al consultar los derechos de reproducción y copia, obtendrá resultados más precisos estableciendo primero los parámetros de entorno.</span><span class="sxs-lookup"><span data-stu-id="0d968-149">When querying for play and copy rights, you will get more accurate results by first setting environmental parameters.</span></span> <span data-ttu-id="0d968-150">Use el método [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) para establecer los parámetros de entorno.</span><span class="sxs-lookup"><span data-stu-id="0d968-150">Use the [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) method to set the environmental parameters.</span></span> <span data-ttu-id="0d968-151">Los resultados de las consultas para el derecho de grabación no se ven afectados por los parámetros del entorno. puede usar los valores predeterminados de forma segura.</span><span class="sxs-lookup"><span data-stu-id="0d968-151">The results of queries for the burn right are unaffected by the environmental parameters; you can safely use the defaults.</span></span>

<span data-ttu-id="0d968-152">Los resultados devueltos por el método **QueryActionAllowed** se agregan a partir de cero o más licencias en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="0d968-152">The results returned by the **QueryActionAllowed** method are aggregated from zero or more licenses in the local license store.</span></span> <span data-ttu-id="0d968-153">El método no puede buscar en todas las licencias que se aplican al identificador de clave si encuentra un resultado habilitado.</span><span class="sxs-lookup"><span data-stu-id="0d968-153">The method may not search all of the licenses that apply to the Key ID if it encounters an enabled result.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d968-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d968-154">Requirements</span></span>



| <span data-ttu-id="0d968-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d968-155">Requirement</span></span> | <span data-ttu-id="0d968-156">Value</span><span class="sxs-lookup"><span data-stu-id="0d968-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d968-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d968-157">Header</span></span><br/>  | <dl> <span data-ttu-id="0d968-158"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d968-158"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d968-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d968-159">Library</span></span><br/> | <dl> <span data-ttu-id="0d968-160"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d968-160"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d968-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d968-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d968-162">**Interfaz IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="0d968-162">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="0d968-163">**Consulta de información de derechos simples**</span><span class="sxs-lookup"><span data-stu-id="0d968-163">**Querying for Simple Rights Information**</span></span>](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





