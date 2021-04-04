---
title: DRM_Rights
description: La \_ propiedad derechos DRM especifica los derechos que necesitará la aplicación en el siguiente intento de abrir un archivo protegido.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077296"
---
# <a name="drm_rights"></a><span data-ttu-id="c196c-104">Derechos de DRM \_</span><span class="sxs-lookup"><span data-stu-id="c196c-104">DRM\_Rights</span></span>

<span data-ttu-id="c196c-105">La **propiedad \_ derechos DRM** especifica los derechos que necesitará la aplicación en el siguiente intento de abrir un archivo protegido.</span><span class="sxs-lookup"><span data-stu-id="c196c-105">The **DRM\_Rights** property specifies the rights that the application will require in the next attempt to open a protected file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c196c-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="c196c-106">Global Constant</span></span>

<span data-ttu-id="c196c-107">g \_ wszWMDRM \_ derechos</span><span class="sxs-lookup"><span data-stu-id="c196c-107">g\_wszWMDRM\_Rights</span></span>

## <a name="data-type"></a><span data-ttu-id="c196c-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c196c-108">Data Type</span></span>

<span data-ttu-id="c196c-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="c196c-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="c196c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c196c-110">Remarks</span></span>

<span data-ttu-id="c196c-111">Se trata de una propiedad de lectura y escritura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) y se establece mediante [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) o [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="c196c-111">This is a read-write property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) and set using either [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) or [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

<span data-ttu-id="c196c-112">En la tabla siguiente se enumeran los derechos admitidos.</span><span class="sxs-lookup"><span data-stu-id="c196c-112">The following table lists the supported rights.</span></span>



| <span data-ttu-id="c196c-113">Right</span><span class="sxs-lookup"><span data-stu-id="c196c-113">Right</span></span>                                           | <span data-ttu-id="c196c-114">Literal de cadena</span><span class="sxs-lookup"><span data-stu-id="c196c-114">String literal</span></span>      | <span data-ttu-id="c196c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c196c-115">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c196c-116">copia de seguridad de g \_ wszWMDRM \_ derecha \_</span><span class="sxs-lookup"><span data-stu-id="c196c-116">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="c196c-117">"Backup"</span><span class="sxs-lookup"><span data-stu-id="c196c-117">"Backup"</span></span>            | <span data-ttu-id="c196c-118">Derecho a realizar una copia de seguridad de la licencia.</span><span class="sxs-lookup"><span data-stu-id="c196c-118">Right to back up the license.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="c196c-119">g \_ wszWMDRM de colaboración de la \_ derecha \_ \_</span><span class="sxs-lookup"><span data-stu-id="c196c-119">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="c196c-120">"CollaborativePlay"</span><span class="sxs-lookup"><span data-stu-id="c196c-120">"CollaborativePlay"</span></span> | <span data-ttu-id="c196c-121">Derecho para reproducir el archivo como parte de una lista de reproducción de colaboración.</span><span class="sxs-lookup"><span data-stu-id="c196c-121">Right to play the file as part of a collaborative playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="c196c-122">g \_ wszWMDRM \_ \_ copia derecha</span><span class="sxs-lookup"><span data-stu-id="c196c-122">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="c196c-123">“Copiar”</span><span class="sxs-lookup"><span data-stu-id="c196c-123">"Copy"</span></span>              | <span data-ttu-id="c196c-124">Derecho para copiar el archivo en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c196c-124">Right to copy the file to a device.</span></span> <span data-ttu-id="c196c-125">Este derecho sustituye a los derechos de copia anteriores (g \_ wszWMDRM la \_ \_ copia derecha \_ a \_ CD, g \_ wszWMDRM la \_ copia derecha a un \_ \_ \_ dispositivo que no es de \_ SDMI \_ y g \_ wszWMDRM \_ \_ copia derecha en el \_ \_ dispositivo de SDMI \_ ).</span><span class="sxs-lookup"><span data-stu-id="c196c-125">This right supersedes the older copy rights (g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD, g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE, and g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE).</span></span> |
| <span data-ttu-id="c196c-126">g \_ wszWMDRM \_ \_ copia derecha \_ a \_ CD</span><span class="sxs-lookup"><span data-stu-id="c196c-126">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="c196c-127">"Print. Redbook"</span><span class="sxs-lookup"><span data-stu-id="c196c-127">"Print.redbook"</span></span>     | <span data-ttu-id="c196c-128">Derecho para copiar el archivo en un CD (formato de libro rojo). En Windows Media DRM 10, este derecho se sustituye por la copia de la derecha de g \_ wszWMDRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c196c-128">Right to copy the file to a CD (Red Book format).In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                             |
| <span data-ttu-id="c196c-129">g \_ wszWMDRM \_ la \_ copia derecha \_ en un \_ dispositivo que no es de \_ SDMI \_</span><span class="sxs-lookup"><span data-stu-id="c196c-129">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="c196c-130">"Transfer. NONSDMI"</span><span class="sxs-lookup"><span data-stu-id="c196c-130">"Transfer.NONSDMI"</span></span>  | <span data-ttu-id="c196c-131">Derecho para copiar el archivo en un dispositivo que no es de SDMI. En Windows Media DRM 10, este derecho se sustituye por la copia de la derecha de g \_ wszWMDRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c196c-131">Right to copy the file to a non-SDMI device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                                  |
| <span data-ttu-id="c196c-132">g \_ wszWMDRM \_ la \_ copia derecha \_ en el dispositivo de \_ SDMI \_</span><span class="sxs-lookup"><span data-stu-id="c196c-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="c196c-133">"Transfer. SDMI"</span><span class="sxs-lookup"><span data-stu-id="c196c-133">"Transfer.SDMI"</span></span>     | <span data-ttu-id="c196c-134">Derecho para copiar el archivo en un dispositivo compatible con SDMI. En Windows Media DRM 10, este derecho se sustituye por la copia de la derecha de g \_ wszWMDRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c196c-134">Right to copy the file to an SDMI-compliant device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                           |
| <span data-ttu-id="c196c-135">g \_ wszWMDRM \_ la \_ reproducción derecha</span><span class="sxs-lookup"><span data-stu-id="c196c-135">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="c196c-136">Reproducción</span><span class="sxs-lookup"><span data-stu-id="c196c-136">"Play"</span></span>              | <span data-ttu-id="c196c-137">Derecho para reproducir el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="c196c-137">Right to play the media file.</span></span>                                                                                                                                                                                        |



 

<span data-ttu-id="c196c-138">Esta propiedad contiene una cadena de caracteres anchos de uno o más derechos separados por signos de punto y coma, por ejemplo: L "reproducción; Copiar CollaborativePlay".</span><span class="sxs-lookup"><span data-stu-id="c196c-138">This property contains a wide-character string of one or more rights separated by semicolons, for example: L"Playback;Copy;CollaborativePlay".</span></span>

## <a name="see-also"></a><span data-ttu-id="c196c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c196c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c196c-140">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="c196c-140">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





