---
title: DRM_LICENSE_STATE_DATA estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de datos de estado de la licencia DRM contiene información sobre las restricciones de licencia de un derecho DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- DRM_LICENSE_STATE_DATA estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709038"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a><span data-ttu-id="b6d40-105">DRM_LICENSE_STATE_DATA estructura (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="b6d40-105">DRM_LICENSE_STATE_DATA structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="b6d40-106">La estructura de datos de estado de la **\_ licencia \_ \_ DRM** contiene información sobre las restricciones de licencia de un derecho DRM.</span><span class="sxs-lookup"><span data-stu-id="b6d40-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains information about the license restrictions for a DRM right.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6d40-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6d40-107">Syntax</span></span>


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a><span data-ttu-id="b6d40-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6d40-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b6d40-109">**dwStreamId**</span><span class="sxs-lookup"><span data-stu-id="b6d40-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="b6d40-110">Número de secuencia al que se aplica la licencia.</span><span class="sxs-lookup"><span data-stu-id="b6d40-110">Stream number to which the license applies.</span></span> <span data-ttu-id="b6d40-111">Debe ser 0, lo que indica que la licencia se aplica a todas las secuencias del archivo.</span><span class="sxs-lookup"><span data-stu-id="b6d40-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="b6d40-112">**dwCategory**</span><span class="sxs-lookup"><span data-stu-id="b6d40-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="b6d40-113">Categoría de cadena que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="b6d40-113">Category of string to be displayed.</span></span> <span data-ttu-id="b6d40-114">Consulte [**\_ categoría de \_ estado \_ de licencia de DRM**](drmdrm-license-state-category.md) para ver los valores posibles y su significado.</span><span class="sxs-lookup"><span data-stu-id="b6d40-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drmdrm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="b6d40-115">**dwNumCounts**</span><span class="sxs-lookup"><span data-stu-id="b6d40-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="b6d40-116">Número de elementos proporcionados en **dwCount**.</span><span class="sxs-lookup"><span data-stu-id="b6d40-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="b6d40-117">Normalmente, este valor es 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="b6d40-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="b6d40-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="b6d40-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="b6d40-119">Matriz de 0 ó 1 o más valores **DWORD** que representan el número de veces que se puede realizar la acción especificada en **dwCategory** .</span><span class="sxs-lookup"><span data-stu-id="b6d40-119">An array of 0 or 1 or more **DWORD** values that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="b6d40-120">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b6d40-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b6d40-121">**dwNumDates**</span><span class="sxs-lookup"><span data-stu-id="b6d40-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="b6d40-122">Número de elementos proporcionados en **fecha y hora**.</span><span class="sxs-lookup"><span data-stu-id="b6d40-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="b6d40-123">Normalmente no se usan más de dos fechas, por ejemplo, con una licencia válida de una fecha hasta otra.</span><span class="sxs-lookup"><span data-stu-id="b6d40-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="b6d40-124">**fecha y hora \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="b6d40-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="b6d40-125">Una matriz de una o varias estructuras **FILETIME** que representan una o más fechas de la licencia.</span><span class="sxs-lookup"><span data-stu-id="b6d40-125">An array of one or more **FILETIME** structures representing one or more dates in the license.</span></span> <span data-ttu-id="b6d40-126">El significado de una fecha determinada depende del valor de **dwCategory**.</span><span class="sxs-lookup"><span data-stu-id="b6d40-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="b6d40-127">**dwVague**</span><span class="sxs-lookup"><span data-stu-id="b6d40-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="b6d40-128">Cero o más de los siguientes marcadores combinados con **una operación OR** bit a bit:</span><span class="sxs-lookup"><span data-stu-id="b6d40-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="b6d40-129">Marca</span><span class="sxs-lookup"><span data-stu-id="b6d40-129">Flag</span></span>                                    | <span data-ttu-id="b6d40-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6d40-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d40-131">datos de estado de licencia de DRM \_ \_ \_ \_ imprecisos</span><span class="sxs-lookup"><span data-stu-id="b6d40-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="b6d40-132">Si se establece, puede haber más licencias que se apliquen al contenido.</span><span class="sxs-lookup"><span data-stu-id="b6d40-132">If set, there may be more licenses that apply to the content.</span></span> <span data-ttu-id="b6d40-133">La única manera de estar seguro de las licencias individuales que se aplican a un identificador de clave determinado es enumerar las licencias.</span><span class="sxs-lookup"><span data-stu-id="b6d40-133">The only way to be certain about the individual licenses that apply to a given key ID is to enumerate the licenses.</span></span> <span data-ttu-id="b6d40-134">Para ello, llame a [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), pasando el identificador de clave como parámetro bstrKID.</span><span class="sxs-lookup"><span data-stu-id="b6d40-134">To do this, call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing the key ID as the bstrKID parameter.</span></span> <span data-ttu-id="b6d40-135">A continuación, use la interfaz IWMDRMLicense recuperada para examinar las licencias.</span><span class="sxs-lookup"><span data-stu-id="b6d40-135">Then use the retrieved IWMDRMLicense interface to examine the licenses.</span></span> |
| <span data-ttu-id="b6d40-136">Estado de la licencia de DRM \_ \_ datos de \_ \_ OPL \_ presente</span><span class="sxs-lookup"><span data-stu-id="b6d40-136">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="b6d40-137">Si se establece, la licencia incluye los niveles de protección de salida (OPLs) que deben recuperarse y comprobarse con el destino de la salida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6d40-137">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b6d40-138">datos de estado de licencia de DRM \_ \_ \_ \_ SAP \_ presentes</span><span class="sxs-lookup"><span data-stu-id="b6d40-138">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="b6d40-139">Si se establece, el contenido se debe entregar mediante la ruta de acceso de audio segura (SAP).</span><span class="sxs-lookup"><span data-stu-id="b6d40-139">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6d40-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6d40-140">Remarks</span></span>

<span data-ttu-id="b6d40-141">Esta estructura se recupera llamando a **IWMDRMLicenseQuery:: QueryLicenseState**.</span><span class="sxs-lookup"><span data-stu-id="b6d40-141">This structure is retrieved by calling **IWMDRMLicenseQuery::QueryLicenseState**.</span></span>

<span data-ttu-id="b6d40-142">Si **dwCategory** es **el \_ \_ \_ \_ recuento de Estados \_ de licencias de DRM de WM desde \_ hasta**, la matriz de **DateTime** normalmente contendrá dos fechas: una fecha "desde" y una fecha "hasta".</span><span class="sxs-lookup"><span data-stu-id="b6d40-142">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**, then the **datetime** array will typically contain two dates: a "from" date and an "until" date.</span></span> <span data-ttu-id="b6d40-143">También se pueden especificar dos pares de fecha para crear licencias más complejas.</span><span class="sxs-lookup"><span data-stu-id="b6d40-143">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="b6d40-144">Los elementos de la matriz **dwCount** se corresponden con las fechas o intervalos de fechas especificados en la matriz **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="b6d40-144">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="b6d40-145">Si **dwCategory** es **el \_ \_ \_ \_ recuento de Estados \_ de licencias de DRM de WM desde \_ hasta** y **fecha y hora** contiene un par de fechas, **dwCount** contendrá un elemento.</span><span class="sxs-lookup"><span data-stu-id="b6d40-145">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="b6d40-146">Si **DateTime** contiene dos pares de fecha (cuatro elementos), **dwCount** debe contener dos elementos, uno para cada par de fechas.</span><span class="sxs-lookup"><span data-stu-id="b6d40-146">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="b6d40-147">En algunos casos, es posible que los usuarios hayan emitido más de una licencia para un archivo.</span><span class="sxs-lookup"><span data-stu-id="b6d40-147">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="b6d40-148">Por ejemplo, podrían haber adquirido una licencia que permitía cinco jugadas hasta el final del mes y, posteriormente, adquirió una segunda licencia para derechos ilimitados.</span><span class="sxs-lookup"><span data-stu-id="b6d40-148">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="b6d40-149">En tal caso, la marca de \_ datos de estado de la licencia DRM \_ \_ \_ se establece en **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) y el componente DRM usará un algoritmo para determinar el conjunto de derechos más probable que se haya aplicado.</span><span class="sxs-lookup"><span data-stu-id="b6d40-149">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="b6d40-150">Cuando expire una licencia, el componente DRM examinará las licencias restantes y así sucesivamente hasta que hayan expirado todas las licencias.</span><span class="sxs-lookup"><span data-stu-id="b6d40-150">When one license expires, the DRM component will examine the remaining licenses, and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6d40-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6d40-151">Requirements</span></span>



| <span data-ttu-id="b6d40-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6d40-152">Requirement</span></span> | <span data-ttu-id="b6d40-153">Value</span><span class="sxs-lookup"><span data-stu-id="b6d40-153">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d40-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6d40-154">Header</span></span><br/> | <dl> <span data-ttu-id="b6d40-155"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6d40-155"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6d40-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6d40-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6d40-157">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="b6d40-157">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





