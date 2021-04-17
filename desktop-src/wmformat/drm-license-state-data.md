---
title: DRM_LICENSE_STATE_DATA estructura (Drmexternals. h)
description: La estructura de datos de estado de la \_ licencia DRM \_ \_ contiene información de licencia sobre un derecho DRM especificado.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- DRM_LICENSE_STATE_DATA estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705161"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a><span data-ttu-id="a5098-105">DRM_LICENSE_STATE_DATA estructura (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="a5098-105">DRM_LICENSE_STATE_DATA structure (Drmexternals.h)</span></span>

<span data-ttu-id="a5098-106">La estructura de datos de estado de la **\_ licencia \_ \_ DRM** contiene información de [*licencia*](wmformat-glossary.md) sobre un derecho [*DRM*](wmformat-glossary.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="a5098-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains [*license*](wmformat-glossary.md) information about a specified [*DRM*](wmformat-glossary.md) right.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5098-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5098-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="a5098-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5098-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5098-109">**dwStreamId**</span><span class="sxs-lookup"><span data-stu-id="a5098-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="a5098-110">Número de secuencia al que se aplica la licencia.</span><span class="sxs-lookup"><span data-stu-id="a5098-110">Stream number to which the license applies.</span></span> <span data-ttu-id="a5098-111">Debe ser 0, lo que indica que la licencia se aplica a todas las secuencias del archivo.</span><span class="sxs-lookup"><span data-stu-id="a5098-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="a5098-112">**dwCategory**</span><span class="sxs-lookup"><span data-stu-id="a5098-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="a5098-113">Categoría de cadena que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="a5098-113">Category of string to be displayed.</span></span> <span data-ttu-id="a5098-114">Consulte [**\_ categoría de \_ estado \_ de licencia de DRM**](drm-license-state-category.md) para ver los valores posibles y su significado.</span><span class="sxs-lookup"><span data-stu-id="a5098-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="a5098-115">**dwNumCounts**</span><span class="sxs-lookup"><span data-stu-id="a5098-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="a5098-116">Número de elementos proporcionados en **dwCount**.</span><span class="sxs-lookup"><span data-stu-id="a5098-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="a5098-117">Normalmente, este valor es 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="a5098-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="a5098-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="a5098-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="a5098-119">Una matriz de 0 o 1 o más **DWORD** s que representan el número de veces que se puede realizar la acción especificada en **dwCategory** .</span><span class="sxs-lookup"><span data-stu-id="a5098-119">An array of 0 or 1 or more **DWORD** s that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="a5098-120">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="a5098-120">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a5098-121">**dwNumDates**</span><span class="sxs-lookup"><span data-stu-id="a5098-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="a5098-122">Número de elementos proporcionados en **fecha y hora**.</span><span class="sxs-lookup"><span data-stu-id="a5098-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="a5098-123">Normalmente no se usan más de dos fechas, por ejemplo, con una licencia válida de una fecha hasta otra.</span><span class="sxs-lookup"><span data-stu-id="a5098-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="a5098-124">**fecha y hora \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="a5098-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="a5098-125">Una matriz de una o varias estructuras FILETIME que representan una o más fechas de la licencia.</span><span class="sxs-lookup"><span data-stu-id="a5098-125">An array of one or more FILETIME structures representing one or more dates in the license.</span></span> <span data-ttu-id="a5098-126">El significado de una fecha determinada depende del valor de **dwCategory**.</span><span class="sxs-lookup"><span data-stu-id="a5098-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="a5098-127">**dwVague**</span><span class="sxs-lookup"><span data-stu-id="a5098-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="a5098-128">Cero o más de los siguientes marcadores combinados con **una operación OR** bit a bit:</span><span class="sxs-lookup"><span data-stu-id="a5098-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="a5098-129">Marca</span><span class="sxs-lookup"><span data-stu-id="a5098-129">Flag</span></span>                                    | <span data-ttu-id="a5098-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5098-130">Description</span></span>                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5098-131">datos de estado de licencia de DRM \_ \_ \_ \_ imprecisos</span><span class="sxs-lookup"><span data-stu-id="a5098-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="a5098-132">Si se establece, puede haber más licencias que se apliquen al contenido.</span><span class="sxs-lookup"><span data-stu-id="a5098-132">If set, there may be more licenses that apply to the content.</span></span>                                                                                         |
| <span data-ttu-id="a5098-133">Estado de la licencia de DRM \_ \_ datos de \_ \_ OPL \_ presente</span><span class="sxs-lookup"><span data-stu-id="a5098-133">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="a5098-134">Si se establece, la licencia incluye los niveles de protección de salida (OPLs) que deben recuperarse y comprobarse con el destino de la salida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5098-134">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span> |
| <span data-ttu-id="a5098-135">datos de estado de licencia de DRM \_ \_ \_ \_ SAP \_ presentes</span><span class="sxs-lookup"><span data-stu-id="a5098-135">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="a5098-136">Si se establece, el contenido se debe entregar mediante la ruta de acceso de audio segura (SAP).</span><span class="sxs-lookup"><span data-stu-id="a5098-136">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5098-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5098-137">Remarks</span></span>

<span data-ttu-id="a5098-138">Esta estructura se devuelve (encapsulada en una estructura de [**\_ datos de \_ estado \_**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) de la licencia de WM) de una llamada a [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) cuando se especifica una de las propiedades de estado de licencia de DRM.</span><span class="sxs-lookup"><span data-stu-id="a5098-138">This structure is returned (encapsulated in a [**WM\_LICENSE\_STATE\_DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) structure) from a call to [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) when you specify one of the DRM license state properties.</span></span> <span data-ttu-id="a5098-139">Estas propiedades son:</span><span class="sxs-lookup"><span data-stu-id="a5098-139">These properties are:</span></span>

-   [<span data-ttu-id="a5098-140">**\_Reproducción de LICENSESTATE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a5098-140">**DRM\_LicenseState\_Playback**</span></span>](drm-licensestate-playback.md)
-   [<span data-ttu-id="a5098-141">**\_CopyToCD LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="a5098-141">**DRM\_LicenseState\_CopyToCD**</span></span>](drm-licensestate-copytocd.md)
-   [<span data-ttu-id="a5098-142">**\_CopyToSDMIDevice LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="a5098-142">**DRM\_LicenseState\_CopyToSDMIDevice**</span></span>](drm-licensestate-copytosdmidevice.md)
-   [<span data-ttu-id="a5098-143">**\_CopyToNonSDMIDevice LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="a5098-143">**DRM\_LicenseState\_CopyToNonSDMIDevice**</span></span>](drm-licensestate-copytononsdmidevice.md)
-   [<span data-ttu-id="a5098-144">**\_CollaborativePlay LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="a5098-144">**DRM\_LicenseState\_CollaborativePlay**</span></span>](drm-licensestate-collaborativeplay.md)
-   [<span data-ttu-id="a5098-145">**\_Copia de LicenseState de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a5098-145">**DRM\_LicenseState\_Copy**</span></span>](drm-licensestate-copy.md)
-   [<span data-ttu-id="a5098-146">**\_PlaylistBurn LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="a5098-146">**DRM\_LicenseState\_PlaylistBurn**</span></span>](drm-licensestate-playlistburn.md)

<span data-ttu-id="a5098-147">Si **dwCategory** es **el \_ \_ \_ \_ recuento de Estados \_ de licencias de DRM de WM desde \_ hasta,** la matriz de **DateTime** normalmente contendrá dos fechas, una fecha "desde" y una fecha "hasta".</span><span class="sxs-lookup"><span data-stu-id="a5098-147">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL,** then the **datetime** array will typically contain two dates, a "from" date and an "until" date.</span></span> <span data-ttu-id="a5098-148">También se pueden especificar dos pares de fecha para crear licencias más complejas.</span><span class="sxs-lookup"><span data-stu-id="a5098-148">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="a5098-149">Los elementos de la matriz **dwCount** se corresponden con las fechas o intervalos de fechas especificados en la matriz **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="a5098-149">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="a5098-150">Si **dwCategory** es **el \_ \_ \_ \_ recuento de Estados \_ de licencias de DRM de WM desde \_ hasta** y **fecha y hora** contiene un par de fechas, **dwCount** contendrá un elemento.</span><span class="sxs-lookup"><span data-stu-id="a5098-150">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="a5098-151">Si **DateTime** contiene dos pares de fecha (cuatro elementos), **dwCount** debe contener dos elementos, uno para cada par de fechas.</span><span class="sxs-lookup"><span data-stu-id="a5098-151">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="a5098-152">En algunos casos, es posible que los usuarios hayan emitido más de una licencia para un archivo.</span><span class="sxs-lookup"><span data-stu-id="a5098-152">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="a5098-153">Por ejemplo, podrían haber adquirido una licencia que permitía cinco jugadas hasta el final del mes y, posteriormente, adquirió una segunda licencia para derechos ilimitados.</span><span class="sxs-lookup"><span data-stu-id="a5098-153">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="a5098-154">En tal caso, la marca de \_ datos de estado de la licencia DRM \_ \_ \_ se establece en **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) y el componente DRM usará un algoritmo para determinar el conjunto de derechos más probable que se haya aplicado.</span><span class="sxs-lookup"><span data-stu-id="a5098-154">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="a5098-155">Cuando expire una licencia, el componente DRM examinará las licencias restantes y así sucesivamente hasta que hayan expirado todas las licencias.</span><span class="sxs-lookup"><span data-stu-id="a5098-155">When one license expires, the DRM component will examine the remaining license(s), and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5098-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5098-156">Requirements</span></span>



| <span data-ttu-id="a5098-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5098-157">Requirement</span></span> | <span data-ttu-id="a5098-158">Value</span><span class="sxs-lookup"><span data-stu-id="a5098-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5098-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5098-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a5098-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a5098-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a5098-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5098-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a5098-162">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5098-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a5098-163">Versión</span><span class="sxs-lookup"><span data-stu-id="a5098-163">Version</span></span><br/>                  | <span data-ttu-id="a5098-164">SDK de Windows Media Format 7 o versiones posteriores del SDK</span><span class="sxs-lookup"><span data-stu-id="a5098-164">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="a5098-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5098-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5098-166"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5098-166"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5098-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5098-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5098-168">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="a5098-168">**Structures**</span></span>](structures.md)
</dt> </dl>

 

