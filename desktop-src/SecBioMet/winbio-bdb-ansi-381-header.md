---
title: Estructura de WINBIO_BDB_ANSI_381_HEADER (Winbio \_ Types. h)
description: Especifica información acerca de una serie de muestras de huellas digitales o Palm.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- Plataforma de biometría de Windows API de WINBIO_BDB_ANSI_381_HEADER Structure
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685985"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a><span data-ttu-id="dcb37-104">\_Estructura del encabezado WINBIO BDB \_ ANSI \_ 381 \_</span><span class="sxs-lookup"><span data-stu-id="dcb37-104">WINBIO\_BDB\_ANSI\_381\_HEADER structure</span></span>

<span data-ttu-id="dcb37-105">La estructura de **\_ encabezado WINBIO BDB \_ ANSI \_ 381 \_** especifica información sobre una serie de muestras de huellas digitales o Palm.</span><span class="sxs-lookup"><span data-stu-id="dcb37-105">The **WINBIO\_BDB\_ANSI\_381\_HEADER** structure specifies information about a series of fingerprint or palm samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb37-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcb37-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a><span data-ttu-id="dcb37-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dcb37-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="dcb37-108">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="dcb37-108">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-109">Tamaño, en bytes, de esta estructura más el tamaño de todas las estructuras de [**\_ registro WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-record.md) para la huella digital o los ejemplos de Palm capturados por un usuario final.</span><span class="sxs-lookup"><span data-stu-id="dcb37-109">The size, in bytes, of this structure plus the size of all [**WINBIO\_BDB\_ANSI\_381\_RECORD**](winbio-bdb-ansi-381-record.md) structures for the fingerprint or palm samples captured from an end user.</span></span> <span data-ttu-id="dcb37-110">Solo los seis bytes inferiores son válidos.</span><span class="sxs-lookup"><span data-stu-id="dcb37-110">Only the low six bytes are valid.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-111">**FormatIdentifier**</span><span class="sxs-lookup"><span data-stu-id="dcb37-111">**FormatIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-112">Especifica el formato.</span><span class="sxs-lookup"><span data-stu-id="dcb37-112">Specifies the format.</span></span> <span data-ttu-id="dcb37-113">Actualmente, debe ser 0x46495200.</span><span class="sxs-lookup"><span data-stu-id="dcb37-113">Currently, this must be 0x46495200.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-114">**NúmeroDeVersión**</span><span class="sxs-lookup"><span data-stu-id="dcb37-114">**VersionNumber**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-115">Especifica el número de versión.</span><span class="sxs-lookup"><span data-stu-id="dcb37-115">Specifies the version number.</span></span> <span data-ttu-id="dcb37-116">Actualmente, este debe ser 0x30313000, que corresponde internamente a 0.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="dcb37-116">Currently this must be 0x30313000 which corresponds internally to 0.1.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-117">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="dcb37-117">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-118">Estructura [**de \_ \_ formato registrada en WINBIO**](winbio-registered-format.md) que contiene el formato de datos registrado como par de propietario/tipo.</span><span class="sxs-lookup"><span data-stu-id="dcb37-118">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that contains the registered data format as an owner/type pair.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-119">**CaptureDeviceId**</span><span class="sxs-lookup"><span data-stu-id="dcb37-119">**CaptureDeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-120">Contiene el identificador de unidad del dispositivo usado para capturar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="dcb37-120">Contains the unit ID of the device used to capture the sample.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-121">**ImageAcquisitionLevel**</span><span class="sxs-lookup"><span data-stu-id="dcb37-121">**ImageAcquisitionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-122">Especifica el nivel de resolución en el que se captura el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="dcb37-122">Specifies the resolution level at which the sample is captured.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-123">**HorizontalScanResolution**</span><span class="sxs-lookup"><span data-stu-id="dcb37-123">**HorizontalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-124">Especifica la resolución horizontal del examen.</span><span class="sxs-lookup"><span data-stu-id="dcb37-124">Specifies the horizontal resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-125">**VerticalScanResolution**</span><span class="sxs-lookup"><span data-stu-id="dcb37-125">**VerticalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-126">Especifica la resolución vertical del examen.</span><span class="sxs-lookup"><span data-stu-id="dcb37-126">Specifies the vertical resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-127">**HorizontalImageResolution**</span><span class="sxs-lookup"><span data-stu-id="dcb37-127">**HorizontalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-128">Especifica la resolución horizontal de la huella digital capturada o la imagen de Palm.</span><span class="sxs-lookup"><span data-stu-id="dcb37-128">Specifies the horizontal resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-129">**VerticalImageResolution**</span><span class="sxs-lookup"><span data-stu-id="dcb37-129">**VerticalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-130">Especifica la resolución vertical de la huella digital capturada o la imagen de Palm.</span><span class="sxs-lookup"><span data-stu-id="dcb37-130">Specifies the vertical resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-131">**ElementCount**</span><span class="sxs-lookup"><span data-stu-id="dcb37-131">**ElementCount**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-132">Número de registros de dedo o Palm en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="dcb37-132">Number of finger or palm records in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-133">**Unidades de escalado**</span><span class="sxs-lookup"><span data-stu-id="dcb37-133">**ScaleUnits**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-134">Contiene la unidad de medida, 1 para pulgadas y 2 para centímetros.</span><span class="sxs-lookup"><span data-stu-id="dcb37-134">Contains the unit of measure, 1 for inches and 2 for centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-135">**PixelDepth**</span><span class="sxs-lookup"><span data-stu-id="dcb37-135">**PixelDepth**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-136">Especifica el número de bits de un píxel.</span><span class="sxs-lookup"><span data-stu-id="dcb37-136">Specifies the number of bits in a pixel.</span></span> <span data-ttu-id="dcb37-137">Puede ser de 1 a 16 bits por píxel para el color.</span><span class="sxs-lookup"><span data-stu-id="dcb37-137">This can be 1 to 16 bits per pixel for color.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-138">**ImageCompressionAlg**</span><span class="sxs-lookup"><span data-stu-id="dcb37-138">**ImageCompressionAlg**</span></span>
</dt> <dd>

<span data-ttu-id="dcb37-139">Especifica el algoritmo utilizado para comprimir el dedo o la imagen de Palm.</span><span class="sxs-lookup"><span data-stu-id="dcb37-139">Specifies the algorithm used to compress the finger or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="dcb37-140">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="dcb37-140">**Reserved**</span></span>
<span data-ttu-id="dcb37-141"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dcb37-141"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="dcb37-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcb37-142">Requirements</span></span>



| <span data-ttu-id="dcb37-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcb37-143">Requirement</span></span> | <span data-ttu-id="dcb37-144">Value</span><span class="sxs-lookup"><span data-stu-id="dcb37-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb37-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcb37-145">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb37-146">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcb37-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="dcb37-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcb37-147">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb37-148">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcb37-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="dcb37-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcb37-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcb37-150"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcb37-150"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcb37-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcb37-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb37-152">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="dcb37-152">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





