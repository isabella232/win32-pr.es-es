---
title: Constantes de WINBIO_CAPABILITY (Winbio \_ Types. h)
description: Subtipos de sensor de huellas digitales.
ms.assetid: D447273E-2A02-484E-B0E4-69FEADD15797
topic_type:
- apiref
api_name:
- WINBIO_CAPABILITY_SENSOR
- WINBIO_CAPABILITY_MATCHING
- WINBIO_CAPABILITY_DATABASE
- WINBIO_CAPABILITY_PROCESSING
- WINBIO_CAPABILITY_ENCRYPTION
- WINBIO_CAPABILITY_NAVIGATION
- WINBIO_CAPABILITY_INDICATOR
- WINBIO_CAPABILITY_VIRTUAL_SENSOR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16de3f496e5c3723722bb7aae22c81eb27c968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905268"
---
# <a name="winbio_capability-constants"></a><span data-ttu-id="48297-103">Constantes de capacidad de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="48297-103">WINBIO\_CAPABILITY Constants</span></span>

<span data-ttu-id="48297-104">Los siguientes subtipos de sensor de huellas digitales son valores de **\_ funcionalidad de WINBIO** que se pueden usar como máscara de la propiedad para el parámetro *CAPABILITIES* de la estructura de [**\_ \_ esquema de unidad WINBIO**](winbio-unit-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="48297-104">The following fingerprint sensor sub types are **WINBIO\_CAPABILITIES** values that can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="48297-105">Estos se refieren a las capacidades del sensor incorporado.</span><span class="sxs-lookup"><span data-stu-id="48297-105">These refer to the onboard sensor capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="48297-106">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="48297-106">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="48297-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="48297-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_SENSOR"></span><span id="winbio_capability_sensor"></span><dl> <span data-ttu-id="48297-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="48297-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48297-109">El sensor puede capturar datos biométricos.</span><span class="sxs-lookup"><span data-stu-id="48297-109">The sensor can capture biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_MATCHING"></span><span id="winbio_capability_matching"></span><dl> <span data-ttu-id="48297-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="48297-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48297-111">El sensor puede hacer coincidir los datos biométricos con una identidad.</span><span class="sxs-lookup"><span data-stu-id="48297-111">The sensor can match biometric data to an identity.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_DATABASE"></span><span id="winbio_capability_database"></span><dl> <span data-ttu-id="48297-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="48297-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48297-113">El sensor contiene una base de datos incorporada.</span><span class="sxs-lookup"><span data-stu-id="48297-113">The sensor contains an onboard database.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_PROCESSING"></span><span id="winbio_capability_processing"></span><dl> <span data-ttu-id="48297-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="48297-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48297-115">El sensor puede realizar el procesamiento biométrico.</span><span class="sxs-lookup"><span data-stu-id="48297-115">The sensor can perform biometric processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_ENCRYPTION"></span><span id="winbio_capability_encryption"></span><dl> <span data-ttu-id="48297-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="48297-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48297-117">El sensor puede cifrar los datos biométricos.</span><span class="sxs-lookup"><span data-stu-id="48297-117">The sensor can encrypt biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_NAVIGATION"></span><span id="winbio_capability_navigation"></span><dl> <span data-ttu-id="48297-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="48297-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48297-119">El sensor puede actuar como panel del mouse.</span><span class="sxs-lookup"><span data-stu-id="48297-119">The sensor can act as a mouse pad.</span></span> <span data-ttu-id="48297-120">Actualmente no se admite.</span><span class="sxs-lookup"><span data-stu-id="48297-120">This is currently not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_INDICATOR"></span><span id="winbio_capability_indicator"></span><dl> <span data-ttu-id="48297-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="48297-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48297-122">El sensor contiene una luz del indicador.</span><span class="sxs-lookup"><span data-stu-id="48297-122">The sensor contains an indicator light.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_VIRTUAL_SENSOR"></span><span id="winbio_capability_virtual_sensor"></span><dl> <span data-ttu-id="48297-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span><span class="sxs-lookup"><span data-stu-id="48297-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="48297-124">El adaptador de sensor administra su propia conexión al hardware biométrico.</span><span class="sxs-lookup"><span data-stu-id="48297-124">The sensor adapter manages its own connection to the biometric hardware.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="48297-125">Esta constante solo se aplica a Windows 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="48297-125">This constant applies only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="48297-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48297-126">Requirements</span></span>



| <span data-ttu-id="48297-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="48297-127">Requirement</span></span> | <span data-ttu-id="48297-128">Value</span><span class="sxs-lookup"><span data-stu-id="48297-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48297-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48297-129">Minimum supported client</span></span><br/> | <span data-ttu-id="48297-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="48297-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="48297-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48297-131">Minimum supported server</span></span><br/> | <span data-ttu-id="48297-132">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="48297-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                  |
| <span data-ttu-id="48297-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48297-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="48297-134"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="48297-134"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48297-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="48297-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48297-136">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="48297-136">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="48297-137">**esquema de la \_ unidad WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="48297-137">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





